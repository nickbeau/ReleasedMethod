# CRMMe.io

## Table of Contents

- [CRMMe.io](#crmmeio)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Background](#background)
  - [Original Idea](#original-idea)
  - [Concept Development](#concept-development)
  - [Following the Pillars](#following-the-pillars)
  - [The development Process](#the-development-process)
    - [Decision One: Platforms](#decision-one-platforms)
    - [Setting Up the Environment](#setting-up-the-environment)
  - [Authentication](#authentication)
  - [Accessing the Office Graph](#accessing-the-office-graph)
  - [Release Process](#release-process)
  - [Progress](#progress)
  - [Sales & Marketing](#sales--marketing)
    - [Video](#video)
    - [WebSite](#website)
    - [Marketing Tools Budget](#marketing-tools-budget)


## Introduction

This document details a case study on the project CRMM.io. Built using the Released Method, CRMme.io is a real world example of the Released Method and how it can work in real life.

## Background

CRMme was envisioned on the 5 June 2020 at the Hornsby Railway Hotel north of Sydney. During Lunch between [Nick Beaugeard](https://www.linkedin.com/in/nickbeaugeard/), [Luke Butler](https://www.linkedin.com/in/lubutler/) and [Bill Barden](https://www.linkedin.com/in/bill-barden-1b771314/), Bill was complaining about how he had thousands of contacts, but commonly they were locked up in email messages and calendar appointments and never really made it into his contacts list.

## Original Idea

The original idea of Bill's can be summed up in the following sentence:

> "Create a system, that will real emails and calendar messages and create a list of contacts and alow these to be exported to a spreadsheet"

## Concept Development

As lunch continued, the concept continued to evolve and after leaving, they settled on a similar solution, maybe using the Office graph.

## Following the Pillars

As this was a Released project, we decided to follow the Released Method:

* [Management Reporting](management-reporting.md) - We decided to use [GitHub](https://www.github.com) to host the management reporting platform. It is a super rich platform and we have a number of tools which work with it.
  * First is [PowerBI for Github](https://app.powerbi.com/groups/me/getapps/services/pbi-contentpacks.pbiapps-github) provides a ton of useful dashboards and reports based on data in Github.
  * Second is our [Project Documentor](https://github.com/nickbeau/project-documentor) which reports the current status of the project and includes any additional data for management reporting.
* [Software Planning and Development](software-planning.md) - Key to software planning is the KanBan and we used [GitHub Projects](https://github.com/features/project-management/) with the released method extensions to manage the project.
* [Testing and Quality Assurance](testing-qa.md)
* [Release Management](release-management.md) - For Release Management we used [GitHub Actions](https://github.com/features/actions) to automatically build, test and release the software when we attempted to release it into production .
* [Documentation](documentation.md)- Documentation is written in markdown and stored in the documentation folder
* [Selling](sales-kit.md) - We decided on a distinctly freemium model with a simple website and video advert to start, with a facebook and email campaign to get our first beta testers.

## The development Process

The first 7 days of the the project were involved in getting a project up and running. We decided to use Microsoft's Blazor framework with its authentication model to the Microsoft Graph.

### Decision One: Platforms

For the Minimum Viable Product we decided to only support Office 365.

### Setting Up the Environment

We decided to implement a new GitHub Organisation and looked for a domain name. We found CRMme.io and decided that was a super name and we would use that. We setup github.com/crmme and created two repositories;

* App would hold the application and its source code and issues
* crmme.github.io would host the application once it was built from the MAster Branch.

We created two Milestones under App
* Beta 1
* Beta 2

We created a new project under App
* MVP Release

We started coding.

## Authentication

The very first hurdle was to create a client-side blazor webassembly application that would successfully authenticate with Office 365. Blazor is new, and the documentation is still growing. However the process documented at the [Microsoft Documentation](https://docs.microsoft.com/en-us/aspnet/core/security/blazor/webassembly/standalone-with-azure-active-directory?view=aspnetcore-3.1) seemed to work and after some testing, we had a Blazor Application that would authenitcate to Office 365.

## Accessing the Office Graph

Not so well documented was how to access the Office Graph. To do this we needed to add some code to our Blazor Pages:

At the top of the .razor file
```razor
@using Microsoft.AspNetCore.Components.WebAssembly.Authentication
@inject IAccessTokenProvider TokenProvider
@inject SignOutSessionStateManager SignOutManager
@inject AuthenticationStateProvider AuthenticationStateProvider
```

And in the code

```cs
tokenResult = await TokenProvider.RequestAccessToken(
    new AccessTokenRequestOptions
    {
        Scopes = new[] { "https://graph.microsoft.com/Calendar.Read" 
    }});


if (tokenResult.TryGetToken(out var token))
{
 //DO WORK HERE
}       
```

Once we had that model worked out, we could begin working with the Microsoft Graph.

## Release Process

We wanted the release process to be as simple as possible, so the following .yaml file drives github actions to compile, build and test our software and then release it.

```yaml
name: .NET Core

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Setup .NET Core
      uses: actions/setup-dotnet@v1
      with:
        dotnet-version: 3.1.300
    - name: Install dependencies now
      run: dotnet restore
    - name: Build
      run: dotnet build --configuration Release --no-restore
    - name: Publish
      run: dotnet publish -c Release
    - name: Test
      run: dotnet test --no-restore --verbosity normal
    - name: Publish artifacts
      uses: actions/upload-artifact@v2
      with:
        name: blazorapp
        path: App/bin/Release/netstandard2.1/publish/wwwroot
  deploy:
    needs: [build]
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
        with:
          persist-credentials: false
          
      - name : download artifacts
        uses: actions/download-artifact@v1
        with:
          name: blazorapp
      - name: Deploy
        uses: JamesIves/github-pages-deploy-action@releases/v3
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          BRANCH: master
          ACCESS_TOKEN: ${{ secrets.PERSONAL_KEY }}
          FOLDER: "blazorapp"
          REPOSITORY_NAME: crmme/crmme.github.io
          TARGET_FOLDER: /
```

## Progress

Now we have an application that can talk to the Office Graph, can be published and tested at will and is fully automated.

Next step is to invite people to join a beta program

## Sales & Marketing

Selling and Marketing a very early stage startup is very different to selling and marketing a well established product. We like to use stealth marketing techniques and not be too salesey. In fact we need customer feedback to make our product work, so we need to be able to put it all together.

### Video

Seems that today, you need video. We put one together in about an hour using:

* [Camtasia](https://www.techsmith.com/video-editor.html) - Always my go-to for video editing, Camtasia is quick and I know it really well. It's also amazing for putting together product demos and presentations. I've used it for about 20 years.
* [Assets for Camtasia](https://library.techsmith.com/camtasia) - The Camtasia Asset library is an amazing and cost effective place to get video, audio and photo assets for Camtasia.
* [Speechelo](https://speechelo.com/?hop=myketodiit) - While the website seems quite scammy, the product works well.

You can judge for yourself:

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/V6MST3OZubo" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

### WebSite
We needed a website, quick and simple. [Wix](www.wix.com) came to the rescue. This platform has so many features, it can handle our Beta Program, mailins and more.

### Marketing Tools Budget

| Item | Cost |
| ---- | ----: |
| Camtasia | $420.98 |
| Assets for Camtasia | $352.43 |
| Speechelo Pro | $379.01 |
| Wix Website | $178.29 |
| Domain (GoDaddy) | $183.43 |
| **TOTAL** | **$1,514.14** |







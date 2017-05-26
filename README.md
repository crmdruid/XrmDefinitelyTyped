# XrmDefinitelyTyped [![NuGet version](https://badge.fury.io/nu/Delegate.XrmDefinitelyTyped.svg)](https://badge.fury.io/nu/Delegate.XrmDefinitelyTyped)

XrmDefinitelyTyped generates [TypeScript](http://www.typescriptlang.org/) 
declaration files based on *your* Dynamics 365/CRM/xRM solution.

It is the TypeScript equivalent of [CrmSvcUtil](https://msdn.microsoft.com/en-us/library/gg327844.aspx), but instead of 
generating early-bound .NET classes for server-side code, it generates TypeScript interfaces for all your client-side coding.

[Read more here](http://delegateas.github.io/Delegate.XrmDefinitelyTyped/)


## Getting started

* [Getting started](http://delegateas.github.io/Delegate.XrmDefinitelyTyped/getting-started.html)
* [Arguments and usage](http://delegateas.github.io/Delegate.XrmDefinitelyTyped/tool-usage.html)


## Contribute


### Build

Recommended environment: [Visual Studio 2017](https://www.visualstudio.com/downloads/)

**Requirements:**

* [F# 4.0+](https://www.microsoft.com/en-us/download/details.aspx?id=48179)
* [TypeScript 2.0+](https://www.microsoft.com/en-us/download/details.aspx?id=48593)
* [Java JRE/SDK](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) (to minimize JavaScript code with closure)

**Building the project**

This project is created from [ProjectScaffold](http://fsprojects.github.io/ProjectScaffold/index.html), 
which uses [FAKE](http://fsharp.github.io/FAKE/) to automate a lot of the build tasks (setup, build, test, docs, nuget package, releases, etc).

Before you can build/run the project from Visual Studio, you need to run `build` from the command-line in the root folder. 
This will trigger the default FAKE build. FAKE handles setting up the project and it's dependencies as needed, before running the actual MSBuild task on the project. 
Once it has been set up correctly by FAKE, you will be able to build the project using Visual Studio from then on.


### Test

Recommended environment: [Visual Studio Code](https://code.visualstudio.com/)

**Requirements:**

* [Node.js and npm](https://nodejs.org/)

#### Run tests

Run `build test` in the root folder of the project to let FAKE handle the setting up, building, running and testing of the project.

To manually run the tests, go to the `test`-folder and execute:

    npm install
    npm test

The typings necessary for the test project to work are generated by running the main XrmDefinitelyTyped project with the current `App.config` file.
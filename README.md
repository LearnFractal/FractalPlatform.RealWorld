# ![RealWorld Example App](logo.png)

> ### Fractal Platform codebase containing real world examples (CRUD, auth, advanced patterns, etc) that adheres to the [RealWorld](https://github.com/gothinkster/realworld) spec and API.

### [Demo](https://fraplat.com/jupiter/RealWorld)&nbsp;&nbsp;&nbsp;&nbsp;[RealWorld](https://github.com/gothinkster/realworld)

This codebase was created to demonstrate a fully fledged fullstack application built with **Fractal Platform** including CRUD operations, authentication, routing, pagination, and more.

We've gone to great lengths to adhere to the **Fractal Platform** community styleguides & best practices.

For more information on how to this works with other frontends/backends, head over to the [RealWorld](https://github.com/gothinkster/realworld) repo.

# Compare to other Frameworks/Solutions

We created special [RealWorldComparator](https://fraplat.com/jupiter/RealWorldComparator) web app 
to compare other FE/BE/Fullstack solutions with Fractal Platform solution.

At the moment this is smallest fullstack solution in 34kb of sources: 
| File Extension | Length |
|----------------|--------|
| .html          | 20 kb  |
| .cs            | 9 kb   |
| .json          | 5 kb   |

# How it works

[Fractal Platform](https://github.com/LearnFractal/FractalPlatform) is low code platform to build [numerous](https://fraplat.com/jupiter/ListOfProjects) different web applications with clean architecture in short time.

[RealWorld (conduit)](https://github.com/LearnFractal/FractalPlatform.RealWorld) application contains only three parts:
- [Layouts](https://github.com/LearnFractal/FractalPlatform.RealWorld/tree/main/Layouts) Html templates of our web application. Html is not mixed with other code and can be provided by UI designers.
- [C# backend](https://github.com/LearnFractal/FractalPlatform.RealWorld/blob/main/RealWorldApplication.cs) All backend logic is placed in one .cs file with 331 lines of code.
- [Database](https://github.com/LearnFractal/FractalPlatform.RealWorld/tree/main/Database) The database is represented as a set of JSON files. Some of the JSON files describe dimensions such as [validation](https://github.com/LearnFractal/FractalPlatform.RealWorld/blob/main/Database/Post/Validation/Document/0000000000.json), [security](https://github.com/LearnFractal/FractalPlatform.RealWorld/blob/main/Database/Dashboard/Security/Document/0000000000.json), [UI](https://github.com/LearnFractal/FractalPlatform.RealWorld/blob/main/Database/Dashboard/UI/Document/0000000000.json), etc.

In the Fractal Platform, we do not mix different layers with each other, and we have achieved next andvantages:
- **Clean architecture**. HTML is HTML. The database is the database. Validation is validation. C# code is C# code. We don't mix different aspects of functionality in one file (e.g., dynamic HTML in a JS file or validation logic in HTML tags).
- **Flexible architecture**. In many cases, we can add or remove features from our application without significant changes to the code.
- **Less code**. Web applications contain approximately [~5-50 less of code](https://fraplat.com/jupiter/RealWorldComparator) than typical web solutions.
- **Easy to read code**. The code consists only of HTML, JSON, and C# files with a simple structure.
- **Easy to deploy**. The RealWorld application can be deployed to Fractal Cloud within a few seconds by simply running the FractalPlatform.Deployment console application.
- **Good performance of web apps**. The web application works quickly because the engine and database have numerous optimizations for rendering the applications.

And we have some disadvantages:
- We don't use REST or web page routing to provide communication between Frontent and Backend parts of our Fullstack web application,
  because by our opinion it has no significant impact on user experience.
  
# Getting started

- Install [Visual Studio Community](https://visualstudio.microsoft.com/vs/community/) or other IDE which supports .NET code
- Install [.NET Core 8.0](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- Download/Clone [Fractal Platform](https://github.com/LearnFractal/FractalPlatform) solution
- Open FractalPlatform_Examples.sln solution in IDE
- Switch to [FractalPlatform.Deployment](https://github.com/LearnFractal/FractalPlatform/tree/main/FractalPlatform.Deployment) project and set "AppNames":["RealWorld"] key in [appsettings.config](https://github.com/LearnFractal/FractalPlatform/blob/main/FractalPlatform.Deployment/appsettings.json) config. Ensure that DeploymentKey in this config is right.
- Run [FractalPlatform.Deployment](https://github.com/LearnFractal/FractalPlatform/tree/main/FractalPlatform.Deployment) project to deploy RealWorld application in Fractal Cloud.
  After deploying RealWorld application will be opened in the your default web browser as https://fraplat.com/jupiter/RealWorld.

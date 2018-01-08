# DEMO

## Creating SAFE project

* Create dir
* `dotnet new -i SAFE.Template`
* `dotnet new SAFE --Fulma --Remoting`
* `code .`
* `build run`
* While the build is running, tell more about Fulma and Remoting, and about project structure

## View 

* Replace "SAFE Template" with "SAFE Demo"
* Replace safeComponents with "Score the talk"
* Remove safeComponents
* Add logo: Level.level -> Level.item -> Image.image -> img (imgSrc depending on context)
* (git history)
* place some text in input to show that HMR preserves state (need to have model state?)

Next: Overall smileys
## ELM-Arch?
## Shared code?


Agenda :

* Brief intro
* Tech Stack
  * Suave.IO
  * (Azure)?
  * Fable
  * Elmish
  * React
  * Redux time travel debugger
  * Fulma (Bulma)
  * F#
* dotnet new SAFE 
* `build run` - while running, explain stuff

To show:

* Explain Elm-architecture

* HMR
* Time-travel debugger
* Console trace
* Server refresh
* Shared code
* Server-side + client-side validation
* React-devtools (for better UI debugging) ? - what fancy can you do with that?
* Redux-devtools (time travel debugger)
* Debugging server side?
* Web App for Containers (Docker) - do manually, not from template?

* Deploying to Docker Hub + Azure - takes time, spend it to show some slides
* http://goqr.me/
* 
* ?Azure Storage

To resolve:

* What domain to show? Presentation feedback - demo deploy actual app? (generate QR code for audience to scan)
* Time travel debugger how it works
* Warning: C:/Users/BRE44821/.nuget/packages/fulma/1.0.0-beta-005/fable/Elements/Heading.fs
C:/Users/BRE44821/.nuget/packages/fulma/1.0.0-beta-005/fable/Elements/Heading.fs(92,8): (92,9) warning FABLE: Looks like Fulma.Elements.Heading.p uses point-free style, this may create problems in runtime, please declare all arguments explicitly.
 @ ./App.fs 19:0-115
 @ ./Client.fsproj
 @ multi (webpack)-dev-server/client?http://localhost:8080 webpack/hot/dev-server ./Client.fsproj 
 --> https://github.com/MangelMaxime/Fulma/pull/83 

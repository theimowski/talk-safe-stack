# DEMO

## Creating SAFE project

* Create dir
* `dotnet new -i SAFE.Template`
* `dotnet new SAFE --Fulma --Remoting`
* `code .`
* `build run`
* While the build is running, tell more about Fulma and Remoting, and about project structure

## Architecture

* Shared code - counter type + Fable.Remoting - not restful, but just fine for our case
* Server side - how init counter works, webpart
* Client side - all compiled to fable, elmish architecture explained

## Building form 

* model init update in App.fs
* Replace "SAFE Template" with "SAFE Demo"
* Replace safeComponents with "Score the talk"
* Remove safeComponents
* Add logo: Level.level -> Level.item -> Image.image -> img (imgSrc depending on context)
* (git history)
* define onInput wih JsInterop; add comment to model4
* add model to name
* place some text in input to show that HMR preserves state

## Client side debugging

* Console trace
* Redux-devtools (Time-travel debugger)
* React-devtools - is outlined on smileys

## Talking to server side 

* Submitting vote - disabling controls on Loading
* Adding protocol to Fable.Remoting
* Server refresh (dotnet watch)
* Firing request in Client side
* Displaying results

NEXT: deploy?

## Deploy

* script, but also F# with FAKE

---

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

---

To show:

* Explain Elm-architecture
 
* HMR

* Console trace
* Redux-devtools (time travel debugger)
* React-devtools (for better UI debugging) ? - what fancy can you do with that?

---

* Server refresh
* Shared code
* Server-side + client-side validation
* Debugging server side?
* Web App for Containers (Docker) - do manually, not from template?

* Deploying to Docker Hub + Azure - takes time, spend it to show some slides
* http://goqr.me/
* 
* ?Azure Storage

To resolve:

* Template - view in separate file?
* Template - rename "Program" to "Server", "App" to "Client"
* What domain to show? Presentation feedback - demo deploy actual app? (generate QR code for audience to scan)
* Time travel debugger how it works
* Warning: C:/Users/BRE44821/.nuget/packages/fulma/1.0.0-beta-005/fable/Elements/Heading.fs
C:/Users/BRE44821/.nuget/packages/fulma/1.0.0-beta-005/fable/Elements/Heading.fs(92,8): (92,9) warning FABLE: Looks like Fulma.Elements.Heading.p uses point-free style, this may create problems in runtime, please declare all arguments explicitly.
 @ ./App.fs 19:0-115
 @ ./Client.fsproj
 @ multi (webpack)-dev-server/client?http://localhost:8080 webpack/hot/dev-server ./Client.fsproj 
 --> https://github.com/MangelMaxime/Fulma/pull/83 

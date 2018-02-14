# Demo Steps

## Creating SAFE project

* `dotnet new -i SAFE.Template`
* `dotnet new SAFE --help`
* `dotnet new SAFE --Fulma landing --Remoting --Docker --language F#`
* `code .`
* `build run`

## Architecture

* while project is building, talk about architecture

## Building form

* remove CSS padding for subtitle
* replace title with "SAFE Demo", subtitle with "Score my talk @..."
* remove `safeComponents`
* add event image (Level -> item -> Image -> img -> Src), scale it to 64x64
* remove contents of `containerBox` and `show` function
* open `Fulma.Elements.Form`, add field helper function
* add comment (Textarea) and name (Input.text)
* add submit (Button.a), make it primary color + full width
* add score type
* add scores field: Level (ismobile) -> column item -> button.a -> `Icon.faIcon [ ] [ Fa.icon Fa.I.SmileO ]`
* add 2x (`Fa.fa2x` to contents), color and outlined to button
* add function `scoreColor`
* add function `scoreIcon` - if time's good play with icons

## Client side debugging

* change Model, Msg, init (comment out cmd for later) and update
* `open Fable.Core.JsInterop`
* `let onInput action = OnInput (fun e -> action !!e.target?value)`
* bind comment, name and score
* demonstrate client side debug - console, HMR, redux, react

## Talking to server side 

* add `Submit` to Msg
* add `Loading` to Model, init
* update function
* bind submit button
* disable all inputs when loading
* move `Score` to Shared
* add Vote and VotingProtocol types in Shared
* Server: `let votes = System.Collections.ConcurrentBag<Vote>()`
* add `countVotes function`, `vote` async function with 1000 sleep
* change adapter to use voting WebPart instead of counter
* replace counting protocol with voting in client
* add `Results` to model, init
* add `mkVote` function
* add `GotResults` to Msg, update (use commented out cmd from init)

.... showing results

## Deploy

* build.fsx: change docker user and image name, copy image name
* Copy and adjust Deploy target
* `build deploy`
* create repository in docker hub
* create web app in azure

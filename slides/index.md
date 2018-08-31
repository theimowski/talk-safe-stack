- title : SAFE apps with F# web stack
- author : Tomasz Heimowski
- theme : night
- transition : default

***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />

# apps

## with <span style="color: #e7ad52;">F#</span> web stack

Tomasz Heimowski http://theimowski.com

<img src="images/twitter.png" style="width:48px; background: transparent; border: none; box-shadow: none"  />
<img src="images/github.png" style="width:48px; background: transparent; border: none; box-shadow: none"  /> 

*@theimowski*

***

## Agenda

* F#
* SAFE
* **Demo**
* Q&A

Slides available at 

http://theimowski.com/talk-safe-stack

***

- data-background : images/confused.gif

# Disclaimer


***

# My goal

***

# F#

![F#](images/fsharp256.png)

* Microsoft origin, OSS
* **General** purpose
* Functional-first
* .NET / Mono / .NET Core / Web **browser**
* https://fsharp.org/

***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />

# ???

***

![Mean](images/mean.png)

<small>https://www.troofal.com/services/mean-stack</small>

***

![LAMP](images/lamp.jpg)

<small>https://www.programmableweb.com/news/what-mean-stack-and-why-it-better-lamp/analysis/2015/12/22</small>

***

![LAMP](images/lamp_better.jpg)

<small>https://www.unixmen.com/how-to-install-lamp-stack-ubuntu-17-04</small>

***

![PHP_LOL](images/twitter_php.png)

<small>https://twitter.com/krisajenkins/status/903988761171820544</small>

***

- data-background : images/4CATS.jpg

<br/>
<br/>
<br/>
<br/>
<br/>

## CATS

### (Typical MS Stack)

<img src="images/CSHARP.jpeg" style="width: 200px; background: transparent; border: none; box-shadow: none"  />
<img src="images/ASPNET.gif" style="width: 200px; background: white; border: none; box-shadow: none"  />
<img src="images/TYPESCRIPT.svg" style="width: 200px; background: none; border: none; box-shadow: none"  />
<img src="images/SQLSERVER.png" style="width: 200px; background: white; border: none; box-shadow: none"  />



***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />

## big picture

</br> 

* Web stack
* Combines several OSS projects
* F# end-to-end
* Type-SAFE
* Cloud-ready
* Flexible

https://safe-stack.github.io

***

<img src="images/safe_s.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">S</span> for <span style="color: #e7ad52;">S</span>aturn<span>

<img src="images/saturn.png" style="background: transparent; border: none; box-shadow: none" width="100" />

https://saturnframework.org/

* **Web server**
* ASP.NET Core, Kestrel
* MVC pattern

***

<img src="images/safe_a.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">A</span> for <span style="color: #e7ad52;">A</span>zure <span>

<img src="images/azure.png" style="background: transparent; border: none; box-shadow: none" width="180" />

https://azure.microsoft.com

* **Cloud** provider

***

<img src="images/safe_f.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">F</span> for <span style="color: #e7ad52;">F</span>able <span>

<img src="images/fable_only_letter.png" style="background: transparent; border: none; box-shadow: none" width="100" />

http://fable.io

* F# to **JavaScript compiler**
* Babel JS

***

<img src="images/safe_e.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">E</span> for <span style="color: #e7ad52;">E</span>lmish <span>

<img src="images/elmish.png" style="background: transparent; border: none; box-shadow: none" width="140" />

https://elmish.github.io

* **UI library**
* inspired by Elm

***

<img src="images/safe_stack.png" style="background: transparent; border: none; box-shadow: none" />

***

##  Demo overview

### Simple voting form

***

## Creating SAFE project

#### Prerequisites:

* [.NET SDK 2.1](https://www.microsoft.com/net)
* [FAKE 5](https://fake.build/) as global .NET tool
* [.NET Framework](https://www.microsoft.com/net/download?initial-os=windows) / [Mono](http://www.mono-project.com/) for [Paket](https://github.com/fsprojects/Paket)\*
* [Node.js](https://nodejs.org/)
* [Yarn](https://yarnpkg.com/) or [NPM](https://www.npmjs.com/)

\* removing this dependency is [WIP](https://github.com/fsprojects/Paket/pull/3183)

***

## Creating SAFE project

* Install SAFE template: `dotnet new -i SAFE.Template`
* Create project from template: `dotnet new SAFE`
* Build & run: `fake build --target run`
* Wait for build to finish: app opens up in browser

***

## Architecture

* Shared code
  * [Fable.Remoting](https://github.com/Zaid-Ajaj/Fable.Remoting)
* Server side
  * [Saturn](https://saturnframework.org/)
* Client side
  * [Fable](http://fable.io/)
  * [Elmish](https://fable-elmish.github.io/elmish/)
  * [React](https://reactjs.org/)

***

## Building form

* [Bulma](https://bulma.io/) (CSS Framework)
* [Fulma](https://github.com/MangelMaxime/Fulma) - Bulma bindings for Elmish
* [Landing Bulma Template](https://dansup.github.io/bulma-templates/)
* [Webpack](https://webpack.js.org) + [webpack-dev-server](https://github.com/webpack/webpack-dev-server)

***

## Client side debugging

* Binding in "Elm Architecture" style
* Console trace
* Hot Module Replacement 
* [Redux-devtools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd) (Time-travel debugger)
* [React-devtools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi)

***

## Talking to server side

* [Fable.Remoting](https://github.com/Zaid-Ajaj/Fable.Remoting)
* Server refresh (dotnet watch)
* Triggering calls from Client side

***

## Deploying the app

* Bundle
* Azure Resource Manager (ARM) Template
* Azure App Service

***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />


## Next steps

* [SAFE Docs](https://safe-stack.github.io/docs/) - SAFE in a nutshell
* Example apps
  * [SAFE BookStore](https://github.com/SAFE-Stack/SAFE-BookStore) - More complex + tests
  * [SAFE Nightwatch](https://github.com/SAFE-Stack/SAFE-Nightwatch) - React Native
  * [SAFE ConfPlanner](https://github.com/SAFE-Stack/SAFE-ConfPlanner) - CQRS + Event-Sourcing
* [Server-Side Rendering](https://github.com/fable-compiler/fable-react/blob/master/docs/server-side-rendering.md#five-steps-to-enable-server-side-rendering-in-your-elmish--dotnet-app) - Back-end React
* You?

Slides: http://theimowski.com/talk-safe-stack

***
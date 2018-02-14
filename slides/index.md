- title : SAFE apps with F# web stack
- author : Tomasz Heimowski
- theme : night
- transition : default

***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />

# apps

## with <span style="color: #e7ad52;">F#</span> web stack

Tomasz Heimowski

http://theimowski.com

***

## Agenda

* SAFE - big picture
* Demo overview
* Creating SAFE project
* DEMOSTEPS
* Deploying the app
* Next Steps

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

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />

## big picture

</br> 

* Web stack
* Combines several OSS projects
* F# end-to-end
* Type-safe
* Cloud-ready
* Flexible

https://safe-stack.github.io

***

<img src="images/safe_s.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">S</span> for <span style="color: #e7ad52;">S</span>uave <span>

<img src="images/suave_logo_only.png" style="background: transparent; border: none; box-shadow: none" width="100" />

https://suave.io

* Standalone, lightweight & composable web **server**
* Alternatives:
  * [Giraffe](https://github.com/giraffe-fsharp/Giraffe) (on top of ASP.NET Core), or [Saturn](https://github.com/SaturnFramework/Saturn)
  * [Freya](https://freya.io/) (web-machine like)

***

<img src="images/safe_a.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">A</span> for <span style="color: #e7ad52;">A</span>zure <span>

<img src="images/azure.png" style="background: transparent; border: none; box-shadow: none" width="180" />

https://azure.microsoft.com

* **Cloud** provider from Microsoft
* Alternatives:
  * Amazon Web Services
  * Google Cloud Platform


***

<img src="images/safe_f.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">F</span> for <span style="color: #e7ad52;">F</span>able <span>

<img src="images/fable_only_letter.png" style="background: transparent; border: none; box-shadow: none" width="100" />

http://fable.io

* F# to **JS** compiler powered by [Babel](https://babeljs.io)
* Alternatives:
  * [WebSharper](https://websharper.com/)

***

<img src="images/safe_e.png" style="background: transparent; border: none; box-shadow: none"  />

## <span style="color: #e7ad52;">E</span> for <span style="color: #e7ad52;">E</span>lmish <span>

<img src="images/elmish.png" style="background: transparent; border: none; box-shadow: none" width="140" />

https://fable-elmish.github.io/elmish

* UI library, inspired by Elm
* Alternatives:
  * [WebSharper](https://websharper.com/) models

***

<img src="images/safe_stack.png" style="background: transparent; border: none; box-shadow: none" />

***

##  Demo overview

### Simple voting form

***

## Creating SAFE project

#### Prerequisites:

* [dotnet SDK 2](https://www.microsoft.com/net/core)
* [node.js](https://nodejs.org/)
* [yarn](https://yarnpkg.com/)
* [.NET Framework](https://www.microsoft.com/net/download) or [mono](http://www.mono-project.com/) for build process

***

## Creating SAFE project

* Install SAFE template: `dotnet new -i SAFE.Template`
* Create project from template: `dotnet new SAFE`
* Build & run: `build run`
* Wait for build to finish: app opens up in browser

***

## Architecture

* Shared code
  * [Fable.Remoting](https://github.com/Zaid-Ajaj/Fable.Remoting)
* Server side
  * [Suave](https://suave.io)
* Client side
  * [Fable](http://fable.io/)
  * [Elmish](https://fable-elmish.github.io/elmish/)
  * [React](https://reactjs.org/) under the hood

***

## Building form

* [Webpack](https://webpack.js.org)
* [Bulma](https://bulma.io/) (CSS Framework)
* [Fulma](https://github.com/MangelMaxime/Fulma) - Bulma bindings for Elmish
* [Landing Bulma Template](https://dansup.github.io/bulma-templates/)

***

## Client side debugging

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
* Docker
* Azure

***

<img src="images/safe_top.png" style="background: transparent; border: none; box-shadow: none"  />


## Next steps

* [SAFE BookStore](https://github.com/SAFE-Stack/SAFE-BookStore) - Tests
* [SAFE Nightwatch](https://github.com/SAFE-Stack/SAFE-Nightwatch) - React Native
* [SAFE ConfPlanner](https://github.com/SAFE-Stack/SAFE-ConfPlanner) - CQRS + Event-Sourcing
* You?

***
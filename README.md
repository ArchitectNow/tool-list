## Introduction

This list was put together for a talk at a St. Louis, MO software development conference called [dev up 2018](http://www.devupconf.org).  The talk is called "Developer Potluck: Useful tools, APIs, services, and other toys every developer should know about".   This is not intended to be construed as an exhaustive list but instead covers a wide variety of tools, technologies, frameworks, and apps that the ArchitectNow team has found useful in the last 12-24 months.  If you know of alternatives or other items we should consider PLEASE let us know.  EVERY item on this list is something we stumbled across randomly or was recommended to us from a peer or customer.   Those recommendations have been extremely valuable to our team and we hope at least something in the list below is valuable to you.

-Kevin Grossnicklaus
President
ArchitectNow
kvgros@architectnow.net

## External APIs

### Algolia

[https://www.algolia.com/](https://www.algolia.com/)

[Example Page using Algolia](https://preview.algolia.com/instantsearch/)
	
Algolia is an API that providies robust search capabilities.  We use it frequently in our applications for realtime searching of content.   Essentially we store a copy of some searchable subset of our data in algolia and their API provides extremely fast and flexible searching of that content.   They provide robust faceting, typo tolerance, lightning fast "Google"-like speed and a ton of SDK's to utilize from many platforms.

### CosmicJS

[https://cosmicjs.com/](https://cosmicjs.com/)

CosmicJS is a headless content management system (CMS) that we use on a number of projects.  Cosmic allows us to easily provide customers with the ability to manage specific content without the need for us to custom develop a set back-end administration pages.   Think of it as similar to using the admin pages of WordPress but not the front-end.   Cosmic stores content by keys and provides administrators with the ability to manage that content.  We use an API to query it and display it accordingly in our applications.


### LOB

[https://lob.com/](https://lob.com/)

LOB is a suite of API's that perform mailing and address verification services.   You can make an API call and send them an image (or multiple) and a physical address and (for a nominal fee) they will print the image onto a postcard, letter, or similar and physically mail to the recipient.  They can do folded letters in envelopes, postcards, etc.   They also have an API we use to send addresses to and they verify it's validity and send us back an updated version (if necessary).   They have some very useful stuff in terms of automating physical mailings.

### Ably

[https://www.ably.io/](https://www.ably.io/)

Ably is a publish/subscribe API that we use to streamline communication between our servers and our clients.   Think of socket.io or SignalR type capabilities without the need to manage the clients yourself.  We use Ably frequently to update Angular (or Xamarin) front-ends when a key change has been made to the server.   We can communicate in realtime from the server to the client (or vice versa) via Ably channels without the headache of configuring the infrastructure ourselves.

All dev up 2018 scoreboard monitors are kept in sync via a set of Ably channels.

A competitor (which we've also used successfuly) would be [Pusher](https://pusher.com/).

### Mailgun

[https://www.mailgun.com/](https://www.mailgun.com/)

Mailgun is the API we nearly always leverage to send emails.  Beyond serving as a robust API for sending emails it has a great dashboard for statistics and a web-hook infastructure for detecting opens, clicks, bounces, etc.   You can also receive mail through Mailgun and perform some complex routing.

A competitor would be [SendGrid](http://www.sendgrid.com). 
### Elmah.io

[https://elmah.io/](https://elmah.io/)

We log all of our application exceptions through Elmah's API.  This gives us a common dashboard and notifications.  It isn't necessary a "bug tracking" tool but is an exception logging platform.   

Competitors would be [Raygun](https://raygun.com/) and [tbd as I forget]

### Stripe

[https://stripe.com/](https://stripe.com/)

We utilize Stripe heavily anytime we need to accept credit card or bank account information and charge payments or transfer money.   We do not store any sensitive payment or account information and instead transfer all that information directly to their secure services and utilize them for everything requiring touching money.

Competitors would be [PayPal](http://www.paypal.com) or [Braintree](https://www.braintreepayments.com/).

### Twilio

[https://www.twilio.com/](https://www.twilio.com/)

We utilize Twilio any time we need to send or receive texts, SMS messages, or handle voice calls.   They provide a very powerful set of communication API's to build rich communication applications.

### Vidyard

[https://www.vidyard.com/](https://www.vidyard.com/)

Vidyards provides video hosting and playback capabilities through a very powerful API.  They have production services to perform batched video customization.  We can send them custom data via an API and they will inject the data (usually text or images) into a video and return us a URL.  We have had clients utilize this very effectively in sales and marketing efforts.

## Developer Tools

### Postman

[https://www.getpostman.com/](https://www.getpostman.com/)

Postman is the utility we utilize to test and interact with all APIs we consume on any project.  This includes the APIs written by our teams as well as 3rd party APIs we may be calling.  We generally prefer this tool over any web-based Swagger/OpenAPI interface.   

### Medis

[https://github.com/luin/medis](https://github.com/luin/medis)

Medis is a Mac client for viewing and manipulating data in a Redis cache.  We use Redis frequently in our applications for a variety of purposes and having the ability to visualize and work with the data stored in Redis is critical.

If using Windows you would need an alternative such as [Redis Desktop](https://redisdesktop.com/).

### Studio3t

[https://studio3t.com/](https://studio3t.com/)

Our team uses MongoDB heavily on nearly every project.   Every member of our team has a license to Studio3T to help them work with Mongo data.  Consider Studio3T the "SQL Server Management Studio" equivalent of working with Mongo.

An alternative (provided by the MongoDB corporation) would be [Compass](https://www.mongodb.com/products/compass).

### Kitematic

[https://kitematic.com/](https://kitematic.com/)

Kitematic (now included with the Docker toolbox) is what all of our team uses to manage our local Docker containers.  This includes our own deployments as well as local versions of services we keep running such as Mongo or Redis.

### Parallels

[https://www.parallels.com/](https://www.parallels.com/)

All of our team members work primarily on Macbook Pro's.  When we need to use Windows 10 we have it ready and loaded in Parallels.   The integration between Mac OSx and Windows 10 via Parallels (which runs Windows as a virtual machine) is crazy good.

### Slack

[https://slack.com/](https://slack.com/)

I jokingly tell people that 90% of my business is run on Slack.  I might laugh but it's close to true.  We use Slack for all communication between ourselves, our customers, and even 3rd party systems such as TFS, etc.  

When someone commits code to a Git repo a message pops up in a Slack channel.  

When a build breaks a message shows up in a Slack channel.

When a file is shared with me a message shows up in a Slack channel.

When a customer has feedback on a particular feature a message shows up in a Slack channel.

When someone wants to take a vacation and needs my permission a message shows up in a Slack channel.

See a trend?

### iTerm2

[https://www.iterm2.com/](https://www.iterm2.com/)

We are big into our (Bash) terminals.  As we work on Mac's we love iTerm2.  Most of us have it heavily customized and open nearly 100% of the time (usually split 20 different ways for various reasons).  We like Git integration, Bash integration, customization, etc, etc.  It's crazy how much we care about how our terminals in 2018.  



New developers on our team are provided this [customization guide](https://medium.com/ayuth/iterm2-zsh-oh-my-zsh-the-most-power-full-of-terminal-on-macos-bdb2823fb04c).  It explains how we customize iTerm2 with [OhMyZsh](https://ohmyz.sh/).

If you are using Windows I personally like using [cmder](http://cmder.net/).

### Sourcetree

[https://www.sourcetreeapp.com/](https://www.sourcetreeapp.com/)

Some developers perform all Git work 100% via the command line.  For me it's more like 20%.   I prefer to have a GUI handy and the one I use is primarily Sourcetree by Atlasian.   It let's me visually see the work being done in any Git repo.  It's free and one of the first things I put on a new dev machine.

Another popular alternative is [GitKraken](https://www.gitkraken.com/).

### Azure Storage Explorer

[https://azure.microsoft.com/en-us/features/storage-explorer/](https://azure.microsoft.com/en-us/features/storage-explorer/)

We are a big Azure shop and developers frequently need visibility into its various storage aspects.

### SQL Operations Studio

[https://docs.microsoft.com/en-us/sql/azure-data-studio/download?view=sql-server-2017](https://docs.microsoft.com/en-us/sql/azure-data-studio/download?view=sql-server-2017)

We work on Macbooks but still leverage SQL Server frequently.  We install SQL Server via Docker Images and use SQL Operations Studio (by Microsoft) as our tool for viewing and manipulating the data (on a Mac)

### Brew or Chocolatey

[https://brew.sh/](https://brew.sh/)

[https://chocolatey.org/](https://chocolatey.org/)

If you are attempting to install any of the above software manually you are likely doing it wrong.   We use package managers such as Brew (Mac OSx) or Chocolaty (Windows) to handle most of our installations.  When a new developer starts we have a very automated set of scripts for either of these tools to install all the common tools we think they would need.

I can run a Chocolaty script on a clean Windows installation and an hour later (without intervention) I have Visual Studio, Office, SQL Server, SourceTree, and a dozen or so other tools I need...completely installed and set up to my specifications.  All via a few command line actions.

### Everything by Jetbrains

[https://www.jetbrains.com/](https://www.jetbrains.com/)

We nearly exclusively use Jetbrain's IDEs for our development.  This is the first thing I buy a new developer. 

We use:

**Webstorm** for Javascript/TypeScript development (including all web development work)

**Rider** for all C# work not requiring a full .NET framework.  This includes ASP.NET Core, Xamarin mobile development, and pretty much anything else.  

**IntelliJ** for all Java developemnt

**PHPStorm** for PHP development

It's weird for me to say this but very few ArchitectNow employees have (or need) any Visual Studio licenses.

### Reflector

[http://www.airsquirrels.com/reflector/](http://www.airsquirrels.com/reflector/)

A wireless screen-mirroring application

Mirror your phone, tablet or computer to the big screen without wires or complicated setups. Present, teach or entertain from the palm of your hand. Reflector makes it easier than ever to share your device screen.

## Packages, Libraries, and other Tools

### Rimraf

[https://www.npmjs.com/package/rimraf](https://www.npmjs.com/package/rimraf)

Rimraf is a small and extremely useful NPM package that allows us to quickly delete folder structures with long paths that might otherwise cause issues with the OS (primarily on Windows).  It is one of the first things I put on a new dev machine.

### Angular

[https://angular.io/](https://angular.io/)

We utilize the Angular framework on nearly all of our front-end web development.   Enough has been said about it that I can't cover it all here.

### React

[https://reactjs.org/](https://reactjs.org/)

When not using Angular we use React :) (or is it vice versa?)

We jump between React and Angular every now and then and would encourage every web developer to be familiar with both. 

Enough has been written about it elsewhere we just wanted to include it and point you in the right direction.

### NestJS

[https://nestjs.com/](https://nestjs.com/)

We have started using NestJS heavily on all of our NodeJS back-end APIs.   Using NestJS allows us to use TypeScript and Node/Express to develop powerful APIs very quickly.   This is one of the biggest and most used frameworks we've adopted recently.

### Electron

[https://electronjs.org/](https://electronjs.org/)

Electron is a Node/JavaScript framework for building cross-platform desktop applications.  Electron is the framework that many of your favorite desktop apps are written in (and run on Windows, Mac, and Linux with one codebase).  

Some examples include:

* Visual Studio Code
* Slack
* Github Desktop
* Skype
* GitKraken

### Hangfire

[https://www.hangfire.io/](https://www.hangfire.io/)

When we need to build highly scalable ASP.NET Core APIs we realize that not every endpoint can be syncronous.   For this reason we rely heavily on Hangfire as a library/platform for queing work onto background threads.  It supports a number of persistant stores but we frequently utilize Redis and/or MongoDB.

### Bull

[https://github.com/OptimalBits/bull](https://github.com/OptimalBits/bull)

Everything said above about Hangfire also applies to APIs we write in NestJS/Node.  For these projects we utilize Bull as the queing infrastructure.

### Swagger/OpenAPI

[https://swagger.io/](https://swagger.io/)

Every API we build exposes a Swagger (OpenAPI) UI and is documented via Swagger docs-json.   Nearly any robust API development platform would support exposing all endpoints and documentation via Swagger.

### Yarn

[https://yarnpkg.com/en/](https://yarnpkg.com/en/)

We have switched from utilizing NPM for our package management to Yarn.  It uses the same package repositories but is much faster and provides a lot of additional functionality.

### Prettier

[https://prettier.io/](https://prettier.io/)

We use Prettier to format much of our code.  It's baked into our development process and I have shortcut keys to auto-format any code I come across based on configured Prettier rules.

### ESLint/TSLint

[https://eslint.org/](https://eslint.org/)

[https://palantir.github.io/tslint/](https://palantir.github.io/tslint/)

All of our source code is Lint'ed before checkins (or otherwise very frequently).  Linting helps ensure we are conforming to code-standards and best practices.  Most IDEs (at least any we would use or recommend) will show Linting errors and ensure compliance.

### Webpack

[https://webpack.js.org/](https://webpack.js.org/)

All of our Angular, React, or NodeJS code utilizes Webpack to bundle the modules, source, and other assets together for deployment.  We do a lot of this by manually configuring weback but most modern CLIs help automate the process.

### class-validation

[https://github.com/typestack/class-validator](https://github.com/typestack/class-validator)

class-validator is a very nice NPM package that greatly simplifies the process of validating TypeScript classes against validation rules (specified by attributes).
 It's easily integrated to NestJS APIs and we use it heavily for validating the inputs to our APIs.
 
### FluentValidation

[https://fluentvalidation.net/](https://fluentvalidation.net/)

When developing ASP.NET Core APIs (or other .NET apps) we utilize FluetValidation (via Nuget) to centralize all our validation rules for our view models.   

### Autofac

[https://autofac.org/](https://autofac.org/)

I would encourage every developer to become as familiar as possible with IoC/DI patterns.   We are big believes in the Inversion of Control pattern and our container of choice is freqently Autofac (for .NET).

### Automapper

[https://automapper.org/](https://automapper.org/)

Automapper for .NET greatly simplifies the seperation of our model classes to our viewmodel (DTO) classes.  It seems simple but does play a big part in our large .NET projects and APIs.  dev up speaker Jimmy Bogard develops and maintains this library.

### email-templates

[https://email-templates.js.org/#/](https://email-templates.js.org/#/)

Providing a robust email template engine for new projects is always tricky.  With our NestJS/NodeJS APIs we solely use this library to send/preview our emails.  It's very robust and extensible.

## Misc Useful Websites

### Theme Forest

[https://themeforest.net/](https://themeforest.net/)

To be 100% honest with you...we get a lot of our best UI templates and designs from Themeforest.  Search for 'admin templates' and find hundreds of pre-build UI's for Angular/React/HTML5/etc.  This let's us get right to the meat of development and helps set the expectation with our clients about what a site might generally look like and what the overall navigation/interaction might look like.  Most are heavily optimized for mobile as well (built on Bootstrap or Google Material or something similar)

Our process:

* Evaluate a bunch of custom themes
* Pick one
* Customize heavily
* Deliver quickly


### Pingdom

[https://www.pingdom.com/](https://www.pingdom.com/)

Pingdom is one of many 3rd party services to externally monitor (and ping) your websites to ensure high availbility.  

### Mockaroo

[https://www.mockaroo.com/](https://www.mockaroo.com/)

We use Mockaroo to generate all of our mock/test data on projects.  We generate a TON of test data and use it to seed our databases early in the development process.  This helps ensure we are always seeing performance based on having a lot of data (and not just two sample rows). 

### MyGet

[https://www.myget.org/](https://www.myget.org/)

We utilize MyGet to host our private NPM and Nuget packages.  We have a core set of reusable libraries that save us a lot of time on specific types of projects.  Sometimes we've open-sourced those libraries and pull them in from GitHub and the public NPM or Nuget repos.  Other scenarios have us needing a private repository for hosting these.  When this is the case we use MyGet. 

### Browserstack

[https://www.browserstack.com/](https://www.browserstack.com/)

Browserstack is our go-to tool for cross browser/OS testing of our website and cross-device testing of our mobile apps.  It's liketly that a few ArchitectNow employees have Browserstack open at any given point in the day.

### Lucidcharts

[https://www.lucidchart.com/](https://www.lucidchart.com/)

We utilize Lucidcharts for all our diagramming and UI prototyping needs.  Nearly every product we build is heavily prototypes in Lucidcharts prior to a line of code being written.

### Pluralsight

[https://app.pluralsight.com](https://app.pluralsight.com)

Like every developer in 2018 we are constantly trying to keep up with new technologies.  Lately we have been heavily utilizing video training to help out.  Pluralsight is our go-to site for learning new (and not-so-new) technologies.

Alternatives would be:

* [https://www.lynda.com/](https://www.lynda.com/)
* [https://www.udacity.com/](https://www.udacity.com/)
* [https://www.udemy.com/](https://www.udemy.com/)

### GitFlow

[Gitflow Article](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

We are religious followers of the GitFlow pattern of managing and releasing software.  There are a number of great articles on this concept and the above link is to one of them.  

### App Name Generator

[https://namelix.com](https://namelix.com)

Ever need an app name or a business name?  This handy site will use neural networks to make some great recommendations.  They will even limit the results to names with available domains.

## Request

Do you have other ideas or thoughts on the list above?  Suggestions from peers, conference attendees, team members, etc are what helped us put the above list together.  Please send your comments (or other recommendations) to me at kvgros@architectnow.net.   We'd love to hear what you are using and how it benefits your team or process.  


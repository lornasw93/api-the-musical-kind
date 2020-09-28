# Presenting... API, the Musical Kind 🎵

*Copy of the tech test requirements is included [here](https://github.com/lornasw93/api-the-musicial-kind/blob/master/Interact%20with%20APIs.pdf)*

## Overview 
I **really** enjoyed working on this and spent any time I could on it. It's an expandable project and for my self-development I will absolutely continue to work on it and implement the below list. 🏃‍♀️

### Approach
For about a year, I've been learning the ways of Angular and .NET Core, and more recently I have been playing around with Node.js and thought at first that could be used for the BE project, but it would've taken longer. I immediately jumped at the chance of using both for this tech test. So, I created 2 new projects and added boilerplate bits - by this I mean installing my usual NPM packages for FE and for BE installing Swagger and creating project folders (services etc.). I focused at the start more on the backend, by using both Postman and Swagger I wanted to be at a point where I could retrieve data. Before any data though, I did some very brief research into music APIs and what the capabilities were.
I setup Firebase hosting for FE and created an Azure Web App Service (with CI/CD) for the BE. As the minimal requirement, I implemented code and appropriate API to retrieve the lyric count by artist and song. Once happy, I changed my focus to FE and carried on from there - switching when needed. *#ThatFullStackLife* 

***Thank you for your time and for checking this out.*** 😀

## If I had more time I would have... ⏳
*No particular order, **bold = priority***
* **Generated charts**
* More comparison data
* Filtered search
* Added authentication - Identity Server maybe
* **Added testing (unit, Jasmine)**
* UI / UX more focus
* **Better error handling** 
* Improved page speeds/SEO
	* Lazy loading images
	* Compress images
	* Added meta tags
* To investigate when sometimes the lyrics count 0 when it shouldn't be 🐞 

## However, I have... ✅
*No particular order*
* Developed 2 separate projects (BE, FE) using different tech stacks including hosting
* Created new sub-domain to use
* FE is from scratch, no template
* BE is minimal
* Tested APIs using Postman and Swagger
* Clear and 'pretty' design
* Responsive
* Visual loading spinner added
* SPA
* Combining 2 existing APIs (Deezer, Lyrics OVH)
* Inserted some Lorna personality (I've seen Matrix 1) 
  
![](https://github.com/lornasw93/api-the-musicial-kind/blob/master/frontend.gif)

## Project Setup

### Backend
* Tech stack: NET Core 3.1, Swagger, REST API 
	* Hosting: Azure (App Service, CI/CD)
* URL: [https://api-the-musical-kind-backend.azurewebsites.net/](https://api-the-musical-kind-backend.azurewebsites.net/)
* Swagger URL: [https://api-the-musical-kind-backend.azurewebsites.net/swagger](https://api-the-musical-kind-backend.azurewebsites.net/swagger)
* Repo: [https://github.com/lornasw93/api-the-musical-kind.backend](https://github.com/lornasw93/api-the-musical-kind.backend)

### Frontend
* Tech stack: Angular 9, Bootstrap 
	* Hosting: Firebase
* URL: [https://api-the-musical-kind.lorna.dev](https://api-the-musical-kind.lorna.dev/)
* Repo: [https://github.com/lornasw93/api-the-musical-kind.frontend](https://github.com/lornasw93/api-the-musical-kind.frontend)

### APIs Used
* Deezer
* Lyrics OVH

## Quick Start 
If you are wanting to run locally, please ensure both BE and FE projects are running simultaneously. Or check out the live FE URL above.

### Frontend
Run `npm install` in the *ClientApp* directory and once finished `ng serve --o` it.

### Backend
#### Prerequisites 

You'll need to setup an account to use the Deezer API [here](https://rapidapi.com/deezerdevs/api/deezer-1) and get an API key. My *appsettings.json* file looks like this (with the API key and irreverent bits omitted):
```
{
  "RapidApi": {
    "Key": "############################################"
  } 
}
```
I then get the key using `IConfiguration` in  my service class. Once you've setup your account and copied over the API key, restore Nuget packages, build and run the project. 

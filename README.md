<!-- PROJECT LOGO -->
<br />
<div align="center">
  <h3 align="center">ASP.NET Core 6 Web Api with MYSQL database</h3>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

An example .net core 6 web api created for general use.

<p align="right">(<a href="#top">back to top</a>)</p>

### Built With

This section should list any major frameworks/libraries used to bootstrap your project. Leave any add-ons/plugins for the acknowledgements section. Here are a few examples.

* [.Net Core 6.js](https://docs.microsoft.com/en-us/dotnet/core/whats-new/dotnet-6)

<p align="right">(<a href="#top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple example steps.


### Installation

_Below is an example of how you can instruct your audience on installing and setting up your app. This template doesn't rely on any external dependencies or services._

1. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
2. Use docker to build your image

  ```
  docker build -t aspnetapp .
  docker run -it -p 5000:80 --name aspnetcore aspnetapp
   ```
   
   
<p align="right">(<a href="#top">back to top</a>)</p>

<!-- Developer Notes -->
## Developer Notes

Steps used to create this project.

Create a Dockerfile

  ```
  touch Dockerfile
   ```
   
  ```
  touch dockerignore
   ```
   ```
  dotnet new webapi -o TodoApi
   ```
   
   ```
   code -r ../TodoApi
   ```
   
   ```
   dotnet dev-certs https --trust
   ```
   
   Adding packages
   ```
   dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
   dotnet add package Microsoft.EntityFrameworkCore.Design
   dotnet add package Microsoft.EntityFrameworkCore.SqlServer
   
   ```
   
   Using .Net Tools
   ```
   dotnet tool install -g dotnet-aspnet-codegenerator
   export PATH=$HOME/.dotnet/tools:$PATH
   dotnet aspnet-codegenerator controller -name TodoItemsController -async -api -m TodoItem -dc TodoContext -outDir Controllers
   ```
   
   
   


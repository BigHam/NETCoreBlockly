# NETCoreBlockly
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-4-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->
.NET Core API to Blockly


[![Build Status](https://dev.azure.com/ignatandrei0674/NETCoreBlockly/_apis/build/status/ignatandrei.NETCoreBlockly?branchName=master)](https://dev.azure.com/ignatandrei0674/NETCoreBlockly/_build/latest?definitionId=9&branchName=master)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/ignatandrei/NetCore2Blockly/blob/master/LICENSE)
[![NuGet](https://img.shields.io/nuget/v/NetCore2Blockly.svg)](https://www.nuget.org/packages/NetCore2Blockly)

# What it does
NETCoreBlockly generates [Blockly](https://developers.google.com/blockly) blocks for each of your controller actions. 

Demo at https://netcoreblockly.herokuapp.com/blockly.html ( play with the links from the bottom)

Demo Video at https://www.youtube.com/watch?v=GptkNWjmCzk

# How to install NETCoreBlockly in a .NET Core 3.1  WebAPI / MVC application

## Step 1:
Install https://www.nuget.org/packages/NetCore2Blockly/ by running the following command in the Package Manager Console:
> Install-Package NetCore2Blockly

## Step 2:
Modify Startup.cs by adding
```csharp
public void ConfigureServices(IServiceCollection services)
        {
            //last line
            services.AddBlockly();
        }
public void Configure(IApplicationBuilder app, IWebHostEnvironment env){
        //if you plan to use as html, do not forget app.UseStaticFiles
        //last line
        app.UseBlockly(); 
}
```

## Step 3:

### Recommended:

To see the UI , please add
```csharp
public void Configure(IApplicationBuilder app, IWebHostEnvironment env){
       
       app.UseBlocklyCli();
}
```
 
### Feel free to modify:

Download from [![Build Status](https://dev.azure.com/ignatandrei0674/NETCoreBlockly/_apis/build/status/ignatandrei.NETCoreBlockly?branchName=master)](https://dev.azure.com/ignatandrei0674/NETCoreBlockly/_build/latest?definitionId=9&branchName=master) the blockly.zip  and put all contents in a wwwroot in the root of your site

## Step 4:
Run the application and browse to  /blockly.html

That's all!



## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="http://www.chestiiautomate.ro/"><img src="https://avatars1.githubusercontent.com/u/4983185?v=4" width="100px;" alt=""/><br /><sub><b>Cosmin Popescu</b></sub></a><br /><a href="https://github.com/ignatandrei/NETCoreBlockly/commits?author=cosminpopescu14" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/adriannasui"><img src="https://avatars3.githubusercontent.com/u/8627433?v=4" width="100px;" alt=""/><br /><sub><b>Adrian Nasui</b></sub></a><br /><a href="https://github.com/ignatandrei/NETCoreBlockly/commits?author=adriannasui" title="Documentation">📖</a></td>
    <td align="center"><a href="https://github.com/tudorgbiliescu"><img src="https://avatars3.githubusercontent.com/u/8693567?v=4" width="100px;" alt=""/><br /><sub><b>Tudor Iliescu</b></sub></a><br /><a href="https://github.com/ignatandrei/NETCoreBlockly/commits?author=tudorgbiliescu" title="Code">💻</a></td>
    <td align="center"><a href="https://github.com/robertszabobv"><img src="https://avatars0.githubusercontent.com/u/9404144?v=4" width="100px;" alt=""/><br /><sub><b>robertszabobv</b></sub></a><br /><a href="https://github.com/ignatandrei/NETCoreBlockly/commits?author=robertszabobv" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-enable -->
<!-- prettier-ignore-end -->
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!


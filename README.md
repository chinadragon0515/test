# RESTier
## 1. Introduction
[OData](http://www.odata.org/ "OData") stands for the Open Data Protocol. It was initiated by Microsoft and is now an ISO and OASIS standard. OData enables the creation and consumption of REST APIs, which allow resources, identified using URLs and defined in a data model, to be published and edited by Web clients using simple HTTP requests.

RESTier is a RESTful API development framework for building standardized, OData V4 based REST services on .NET. It can be seen as a middle-ware on top of Web API OData. RESTier can provide convenience to bootstrap an OData service and add business logic in several simple steps like what WCF Data Services (which is sunset) does as well as flexibily and easy customization like what Web API OData does.

For more information about OData, please refer to the following resources:
- [OData.org](http://www.odata.org/)
- [OASIS Open Data Protocol (OData) Technical Committee](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=odata)

**For how to adopt this library to build OData service, please refer to the following resources:**
- [Build an OData v4 Service with RESTier Library](http://odata.github.io/RESTier/#01-01-Introduction)

**For how to adopt .NET OData Client to consume OData service, please refer to the following resources:**
- [OData .Net Client](http://odata.github.io/odata.net/#04-01-basic-crud-operations)

Please be noted that currently RESTier is still a preview version.

## 2. Project structure
The project currently has two branches: [master](https://github.com/OData/RESTier/tree/master), [gh-pages](https://github.com/OData/RESTier/tree/gh-pages).

**master branch**

The master branch has the following libraries:
- [RESTier Core](https://www.nuget.org/packages/Microsoft.Restier.Core/) (namespace `Microsoft.Restier.Core`):<br />The RESTier Core contains framework class like Api related logic, model builder, query summitter, convention based logic.
- [RESTier WebApi Publisher](https://www.nuget.org/packages/Microsoft.Restier.WebApi/) (namespace `Microsoft.Restier.WebApi`):<br />The RESTier WebApi Publisher contains classes to handle OData specified logic with WebAPi OData library.
- [RESTier EntityFramework Provider](https://www.nuget.org/packages/Microsoft.Restier.EntityFramework/) (namespace `Microsoft.Restier.EntityFramework`):<br />The RESTier EntityFramework Provider contains classes and methods that facilitate query summit and execute with EntityFramework library.
- [RESTier Security](https://www.nuget.org/packages/Microsoft.Restier.Security/) (namespace `Microsoft.Restier.Security`):<br />The RESTier Security contains classes and methods for security control, it is in maintained model and ASP .NET WebAPI related security control is recommended now.

For these libraries, we accept bug reports, feature requirements and pull requests. The corresponding fixes and implementations will be included into every new release.


**gh-pages branch**

The gh-pages branch contains documentation source for RESTier - tutorials, guides, etc.  The documentation source is in Markdown format. It is hosted at [RESTier Pages](http://odata.github.io/RESTier "RESTier Pages").

## 3. Building, Testing, Debugging and Release
LocalDB v12.0 or above will be used which is part of VS2015 and no additional installation is needed. The Database will be automatically initialized by the test code if it doesn't exist.

### 3.1 Building and Testing in Visual Studio
Simply open the solution files under 'sln' folder and build them in Visual Studio 2015.

Here is the usage of each solution file:
- RESTier.sln - Product source and all tests. It uses EntityFramework 6.x and built with .Net Framework version 4.5.
- RESTier.EF7.sln - Product source and all tests. It uses EntityFramework 7.x and built with .Net Framework version 4.5.

For running tests, you need to open Visual Studio IDE as **_Administrator_** so that the test services can be started properly.

### 3.2 One-click build and test script in command line
Open Command Line Window with "**Run as administrator**", cd to the root folder and run following command:

```
build.cmd
```

The build and test will take about 4 minutes. Here are some other usages:
- `build.cmd Nightly`. Build and run all nightly test suites.
- `build.cmd SkipStrongName`. Configure strong name skip of RESTier libraries on your machine and build (no test run).
- `build.cmd DisableSkipStrongName`. Disable strong name skip of RESTier libraries on your machine and build (no test run).

### 3.3 Debug
Please refer to the [How to debug](http://odata.github.io/WebApi/10-01-debug-webapi-source).

### 3.4 Official Release
The release of the component binaries is carried out regularly through [Nuget](http://www.nuget.org/).

## 4. Documentation
Please visit the [RESTier pages](http://odata.github.io/RESTier). It has detailed descriptions on each feature provided by RESTier.

## 5. Community
### 5.1 Contribution
There are many ways for you to contribute to RESTier. The easiest way is to participate in discussion of features and issues. You can also contribute by sending pull requests of features or bug fixes to us. Contribution to the documentations is also highly welcomed. Please refer to the [CONTRIBUTING.md](https://github.com/OData/RESTier/blob/master/.github/CONTRIBUTING.md) for more details.

### 5.2 Support
- Issues<br />Report issues on [Github issues](https://github.com/OData/RESTier/issues).
- Questions<br />Ask questions on [Stack Overflow](http://stackoverflow.com/questions/ask?tags=odata).
- Feedback<br />Please send mails to [odatafeedback@microsoft.com](mailto:odatafeedback@microsoft.com).
- Team blog<br />Please visit [http://blogs.msdn.com/b/odatateam/](http://blogs.msdn.com/b/odatateam/) and [http://www.odata.org/blog/](http://www.odata.org/blog/).

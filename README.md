# Introduction

Torizon Uno Platform Integration delivers a better and easy experience for creating Uno Platform solutions using UWP, XAML and C# for Embedded Linux GUI applications.

# Requirements

- OS Supported:
	- Windows 10 Pro / Enterprise / Education
	- Linux (it was validated using Ubuntu 20.04)
- [Toradex Torizon Support Extension for Visual Studio Code](https://developer.toradex.com/knowledge-base/visual-studio-code-development-extension-pythonnet-core)
- [Microsoft C# Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)
- [Uno Platform Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=microhobby.uno-platform)
- [.NET Core 3.1 SDK](https://dotnet.microsoft.com/download)
- [.NET 5 SDK](https://dotnet.microsoft.com/download)
- Toradex Hardware with [TorizonCore](https://developer.toradex.com/software/torizon) installed

> ⚠️ Torizon Uno Platform Integration is only available in the early access version of the [Toradex Torizon Support Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=Toradex.torizon-early-access)

# Features

## Solution Creation

To create a new `Torizon Uno Platform application` type `CTRL+SHIFT+P` to open the command pallet and select the option `Torizon/.NET: Create .NET Core application`:

![](https://docs.toradex.com/109417-01-selectdotnetapplication.gif?v=1)

Next, write the application name on the same command bar, press enter and select a folder to store the solution folder and files that will be created:

![](https://docs.toradex.com/109418-02-projectnameandfolder.gif?v=1)

Next, select the `.NET Uno Application (⚠️ Experimental, from Toradex Labs)` template;

![](https://docs.toradex.com/109419-03-selectdotnetapplicationtemplate.gif?v=1)

Next, select the target's development board architecture:

![](https://docs.toradex.com/109420-04-selectarchitecture.gif?v=2)

And lastly the target's default user, leave it as the `torizon` and press enter:

![](https://docs.toradex.com/109421-05-projectcreation.gif?v=1)

With this the `Torizon Uno Platform application` will be created and the VS Code workspace will be loaded to the folder selected to store the application. Wait for the load of the Uno Platform Extension and Torizon Extension:

![](https://docs.toradex.com/109422-06-loadprojectfirsttime.gif?v=1)

The first time the project is opened in VS Code the XAML symbols are not available to the intellisense, which will result in the C# extension complaining about some errors.

### IntelliSense

For intellisense to work correctly, it is necessary to perform a first build of the solution, to generate the XAML symbols. In the application workspace open any `.xaml` file and click on the `Update XAML Symbols`, command in the top right of navigation tabs:

![](https://docs.toradex.com/109423-07-syncxaml.gif?v=1)

After the finish of the build reload the solution clicking in the `YourProjectName.sln` in the VS Code taskbar and selecting again the `YourProjectName.sln` in the command bar:

![](https://docs.toradex.com/109424-08-reloadomnisharpsolution.gif?v=2)

The reload of solution is required only the first time the project is loaded. The update of XAML symbols is needed for every new control, bind or name added to a `.xaml` file.

## Debug Tools

### Remote Deploy & Debug

To deploy and debug on the target, embedded Linux development board, set some breakpoint on the code and press `F5`:

![](https://docs.toradex.com/109425-09-remotedeploydebug.gif?v=1)

Is possible evaluate variables using the mouse over, `VARIABLES`, `WATCH` and `DEBUG OUTPUT` panel.

#### Remote Hot Reload

During a debug sessions is possible to use the Hot Reload feature. Edit the `.xaml` file been presented on the screen of target, save the changes and check the changes taking place in the application running:

![](https://docs.toradex.com/109426-10-hotreload.gif?v=1)

### Locally Debug & Hot Reload

It is also possible to run the application in Debug mode locally, development PC. In the Debug activity bar there are two target options. The default target `.NET Launch (Torizon)` will deploy, debug and remote hot reload, on a development board with Embedded Linux and Torizon. The target `.NET Launch (Skia Uno Platform)` will run, debug and hot reload locally. Select it and press `F5` to start the debug session locally:

![](https://docs.toradex.com/109427-11-locallydebug.gif?v=1)

During the local debugging session is possible edit the `.xaml` file been presented, save the changes and check the changes taking place in the application running:

![](https://docs.toradex.com/109428-12-locallyhotreload.gif?v=1)



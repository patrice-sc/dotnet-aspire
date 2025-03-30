# dotnet-aspire
The [Windows Dev Environment](https://learn.microsoft.com/en-us/windows/dev-environment/) guide helps developers set up tools like Windows Terminal, WSL, and Visual Studio for efficient coding on Windows.  

[.NET Aspire](https://learn.microsoft.com/en-us/dotnet/aspire/) is a cloud-native development stack designed for streamlined local development and deployment of .NET applications. It simplifies configuration, service discovery, and observability, making it easier to build and run distributed applications locally before scaling to the cloud. Rather than providing ready-to-use code, this repository will focus on a step-by-step approach to adopting **.NET Aspire**, guiding developers through each phase of integrating the stack into their local development workflows.

Assuming you are already developing .NET applications on Windows and have **WSL** installed, we will now cover the installation of **Podman** as an alternative to Docker. While **Docker Desktop** is supported, it may require a paid [license](https://docs.docker.com/subscription/desktop-license/).

In a PowerShell terminal running as Administrator, install Podman CLI and ensure that Podman is used, even if other tools such as [Rancher Desktop](https://rancherdesktop.io/) are installed:
```powershell
winget install RedHat.Podman
[System.Environment]::SetEnvironmentVariable("DOTNET_ASPIRE_CONTAINER_RUNTIME", "podman", "User")
```

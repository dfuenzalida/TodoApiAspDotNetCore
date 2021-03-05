# TodoApi from the "Create a web API with ASP.NET Core" tutorial

This repo contains the TodoApi from the [Create a web API with ASP.NET Core](https://docs.microsoft.com/en-us/aspnet/core/tutorials/first-web-api?view=aspnetcore-5.0&tabs=visual-studio) tutorial and the crude web UI from the [Call an ASP.NET Core web API with JavaScript](https://docs.microsoft.com/en-us/aspnet/core/tutorials/web-api-javascript?view=aspnetcore-5.0).

## Requisites

* [.NET 5.0 SDK or later](https://dotnet.microsoft.com/download/dotnet/5.0)
* Docker, if you want to run the example inside a container instead

## Usage

If you have the .NET 5.0 SDK you can run the Web API with `dotnet run` from the console and opening one of the URLs listed in the console:

```
$ dotnet run
Building...
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: https://localhost:5001
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: http://localhost:5000
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Development
info: Microsoft.Hosting.Lifetime[0]
      Content root path: /home/user/Projects/TodoApi
```

### Container

You can build the container image with: `docker build . -t todoapi:latest`

### Container with VS Code

If you have Visual Studio Code and the Docker extension, you can run it from a container by right-clicking on the `Dockerfile` and selecting `Build Image...` and confirming the default tag `todoapi:latest`.

Once the image is built, you can switch to the Docker extension, expand `todoapi` from the list of images, then right-click on the `latest` image and select `Run`.

From the list of containers, you can select the `todoapi:latest` image that is now running, right-click on it and select `Open in Browser`.

You might need to change the protocol in the URL from `https` to `http` if the port 443 was already busy.

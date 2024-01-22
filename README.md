# Deepstack .NET SDK Samples (Examples of use)

The official [Deepstack .NET library][ds-dotnet] samples

## Usage

Clone this repository

### Sample Console App

Sample console app that showcases all Deepstack SDK service calls (Pending updates).

##### Configuration

All SDK calls in the Sample Console App can be configured using the static `DeepStackConfiguration` object:

```c#
DeepStackConfiguration.PublishableApiKey = "Your Publishable API Key";
DeepStackConfiguration.SharedSecret = "Your Shared Secret";
DeepStackConfiguration.AppId = "Your APP ID";
DeepStackConfiguration.UseSandbox = false; //true if you need to test through Globally Paid sandbox
DeepStackConfiguration.RequestTimeoutSeconds = 90;
```
Or using the `DeepStackConfiguration` *Setup* method:

```c#
DeepStackConfiguration.Setup("Your Publishable API Key", "Your Shared Secret", "Your APP ID", useSandbox: false, requestTimeoutSeconds: 90);
```

##### Run
Run the Sample Console App and see all examples in `Program.cs`

### Sample App

Sample MVC app that showcases charge sale transaction done through a UI credit card form using the Deepstack JS-SDK

##### Configuration

All SDK calls can be configured within `ConfigureServices` method in `Startup` class using the `AddDeepStack` extension.
Additionally, this extension call will register all Deepstack services:

```c#
services.AddDeepStack("Your Publishable API Key", "Your Shared Secret", "Your APP ID", useSandbox: false, requestTimeoutSeconds: 90);
```

To register the Deepstack services only, `AddDeepStackServices` extension can be used:

```c#
services.AddDeepStackServices();
```

Or using the `appSettings.{Environment}.json` file:

```json
  "DeepStack": {
    "PublishableApiKey": "Your Publishable API Key",
    "SharedSecret": "Your Shared Secret",
    "AppId": "Your APP ID",
    "UseSandbox": true,
    "RequestTimeoutSeconds": 90
  }
```

##### Run
Run the Sample MVC App, populate with test data and click `Submit`

---
For any feedback or bug/enhancement report, please [open an issue][issues] or [submit a
pull request][pulls].

[ds-dotnet]: https://github.com/deepstack-payments/deepstack-dotnet
[issues]: https://github.com/deepstack-payments/deepstack-dotnet/issues
[pulls]: https://github.com/deepstack-payments/deepstack-dotnet/pulls
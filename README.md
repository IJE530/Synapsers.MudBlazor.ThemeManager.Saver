# Synapsers.MudBlazor.ThemeManager.Saver 🎨

![GitHub release](https://img.shields.io/github/release/IJE530/Synapsers.MudBlazor.ThemeManager.Saver.svg)
![GitHub issues](https://img.shields.io/github/issues/IJE530/Synapsers.MudBlazor.ThemeManager.Saver.svg)
![GitHub stars](https://img.shields.io/github/stars/IJE530/Synapsers.MudBlazor.ThemeManager.Saver.svg)

Welcome to the **Synapsers.MudBlazor.ThemeManager.Saver** repository! This project enhances the MudBlazor ThemeManager by adding powerful theme saving and persistence features. You can design, customize, save, and manage themes for your Blazor applications seamlessly. The solution utilizes JSON file storage and localStorage integration for automatic persistence.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Links](#links)

## Features

- **Theme Customization**: Easily design and modify themes to match your application’s branding.
- **JSON File Storage**: Save themes in a structured JSON format for easy retrieval and management.
- **LocalStorage Integration**: Automatically save themes to the browser's localStorage for persistence across sessions.
- **Automatic Persistence**: Themes persist without additional user actions, providing a smooth user experience.
- **Blazor Compatibility**: Works with Blazor Server, Blazor WebAssembly, and Blazor Client applications.
- **User-Friendly Interface**: Intuitive design makes it easy for developers to implement and manage themes.

## Installation

To get started, you need to install the package via NuGet. You can do this by running the following command in your project directory:

```bash
dotnet add package Synapsers.MudBlazor.ThemeManager.Saver
```

Alternatively, you can find the package in the NuGet Package Manager in Visual Studio.

## Usage

After installing the package, you can start using the ThemeManager in your Blazor application. Here’s a simple example of how to set it up:

1. **Add the necessary using directive**:

   ```csharp
   using Synapsers.MudBlazor.ThemeManager.Saver;
   ```

2. **Configure the ThemeManager in your `Startup.cs`**:

   ```csharp
   public void ConfigureServices(IServiceCollection services)
   {
       services.AddMudServices();
       services.AddThemeManager();
   }
   ```

3. **Use the ThemeManager in your components**:

   You can now access the ThemeManager in your Blazor components. Here’s a basic example:

   ```razor
   @inject IThemeManager ThemeManager

   <MudThemeProvider Theme="@ThemeManager.CurrentTheme">
       <MudButton @onclick="SaveTheme">Save Theme</MudButton>
   </MudThemeProvider>

   @code {
       private void SaveTheme()
       {
           ThemeManager.SaveCurrentTheme();
       }
   }
   ```

This example demonstrates how to inject the `IThemeManager` and use it to save the current theme. You can further explore the API for more advanced features.

## Contributing

We welcome contributions! If you have ideas for improvements or new features, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes and commit them (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

Please ensure your code adheres to the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Links

For the latest releases, please visit the [Releases](https://github.com/IJE530/Synapsers.MudBlazor.ThemeManager.Saver/releases) section. You can download the latest version and execute it to take advantage of the new features.

If you want to stay updated on new releases and changes, you can check the [Releases](https://github.com/IJE530/Synapsers.MudBlazor.ThemeManager.Saver/releases) section regularly.

## Topics

This repository covers a range of topics relevant to Blazor development, including:

- Blazor
- Blazor Client
- Blazor Components
- Blazor Server
- Blazor WebAssembly
- Component Library
- C#
- Material Design
- .NET Core
- WASM

## Conclusion

Thank you for checking out **Synapsers.MudBlazor.ThemeManager.Saver**. We hope this tool helps you create beautiful and persistent themes for your Blazor applications. If you have any questions or need support, feel free to reach out through the issues section of this repository.
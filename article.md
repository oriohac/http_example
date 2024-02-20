# Beginer Friendly  Implementation of the HTTP Methods(Get, Post, Put and Delete) From API’s in Flutter.

## **Introduction**

HTTP which stands for Hyper-Text Transfer Protocol is a protocol that helps us to communicate over the internet, communication in the sense that we can send data from a source to a destination, retrieve or get data from a source(server), update an existing data and delete it when we wish to. For us to successfully carry out these tasks, we have to relly on some of the HTTP paradigms, which include but not limited to the get method, the post, put, patch, read and delete methods. API which stands for Application Programming Interface can be referred to as data source or location, where structured data are kept which can be accessed from different plartforms for software development, given that you have the right credentials to access the data.

In this article we shall set our focus on the simple ways on how one can implement some of the basic HTTP methods, which includes the get, post, put and delete methods, using Flutter which is a cross-platform framework built with Dart.

### Key takeaways

- Create and Run Flutter project.
- Implement http in a project.
- Consume data from an API.

### Preriquisites:

To follow up this article you need to have these:

- A computer with Flutter setup on it.
- Basic programming knowledge.
- Understand the flutter file structure.
- Working internet.
- Code editor or an IDE(Visual Studio Code or Android Studio)

With these we are set to dive into the application of these methods.

### Table of Contents:

- [Introduction](https://www.notion.so/Beginer-Friendly-Implementation-of-the-HTTP-Methods-Get-Post-Put-and-Delete-From-API-s-in-Flutte-b30582e9201d475e8d9e5bc0207a6894?pvs=21)
- [Key Takeaways](https://www.notion.so/Beginer-Friendly-Implementation-of-the-HTTP-Methods-Get-Post-Put-and-Delete-From-API-s-in-Flutte-b30582e9201d475e8d9e5bc0207a6894?pvs=21)
- [Preriquisites](https://www.notion.so/Beginer-Friendly-Implementation-of-the-HTTP-Methods-Get-Post-Put-and-Delete-From-API-s-in-Flutte-b30582e9201d475e8d9e5bc0207a6894?pvs=21)
- 

To start, we have to create a new flutter project, by following this article it is assumed that you have Flutter set up on your computer, if you have not, you can [follow this link](https://www.flutter.dev) to get Flutter on your computer. Once you have this ready, go into your preffered IDE and open your terminal(ctrl+` opens the terminal on VSCode) type the following in the terminal.

```dart
flutter create http_example
```

This will create a new flutter project, with the required files and folders.

![2024-02-20_06-02.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/f4d89012-b551-4a73-83b8-de61178696e8/dda2f2be-ca5f-45af-b428-0c1fab2bd105/2024-02-20_06-02.png)

Head into the lib folder and open the main.dart file. You can see a demo counter app code, clear it so we can create what we need.

In your project home directory, open the pubspec.yaml file and paste the latest version of the http package for [flutter](http://pub.dev), under dependecies under flutter.

```dart
dependencies:
  flutter:
    sdk: flutter

	http: ^1.2.0
```

In this article I’m using the above version, but make sure to go to [pub.dev](https://www.pub.dev) and copy the latest version of the package. After that, click on the “Get Packages” arrow-down icon at the top righthand corner of vscode to get the package into you project.

The package can also be gotten into our project when we use,

```dart
flutter pub get
```

in the terminal, after we have pasted the package in pubspec.ymal file.

After that now update your lib/main.dart file with the code below, importing the http package.

```dart
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http;

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  
  Widget build(BuildContext context) {
    return MaterialApp(
    );
  }
}
```

### The Get Method:

The get method retrieves resources from a source to the destination, this method is very important, as it helps in several
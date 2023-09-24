# Class 41


# React Native



### [getting started with react native](https://facebook.github.io/react-native/docs/getting-started)



## 1. Name three Core Components of React Native and describe what they do.

- View: A container that supports layout with flexbox, style, some touch handling, and accessibility controls.

- Text: Displays, styles, and nests strings of text and even handles touch events.

- Image: Displays different types of images.

- ScrollView: A generic scrolling container that can contain multiple components and views.

- TextInput: Allows the user to enter text.


## 2. What problem does React Native solve (why call it native)?

React Native solves the problem of building mobile apps for multiple platforms (iOS and Android) with a single codebase, allowing developers to write most of the code in JavaScript while achieving near-native performance and appearance. 

It's called "native" because it enables the development of apps that have a native look and feel while sharing code across platforms.


## 3. What are the building blocks of a React Native app? How does that compare to a React app?

Building Blocks of a React Native app include components, state management, and navigation. This is similar to a React app but tailored for mobile platforms.


### [expo](https://expo.io/)



## 1. What solution does expo provide?

Expo simplifies React Native app development by offering a quick start, unified API, and access to native device features, enabling faster and easier cross-platform mobile app development. It provides a development workflow that includes instant testing on physical devices and abstracts platform-specific complexities.


## 2. Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the ____ workflow.

Managed


## 3. What is the difference between React Native and Expo?

React Native and Expo are both tools used for developing mobile applications with JavaScript and React, but they serve different purposes and offer different levels of abstraction and features. Here are the key differences between React Native and Expo:

#### React Native:

- Framework vs. Toolkit: React Native is an open-source framework developed by Facebook for building mobile applications using JavaScript and React. It provides a foundation for creating cross-platform mobile apps but requires more manual setup and configuration.

- Customization and Native Code: React Native gives developers full control over the native modules and allows them to write custom native code in Java, Swift, or Objective-C when necessary for specific platform features.

- Complexity: React Native offers more flexibility but also comes with a steeper learning curve and potentially more complex development setup, especially for those who need to work with native modules.

#### Expo:

- Toolkit for React Native: Expo is a set of tools and services built on top of React Native, designed to simplify and speed up the development process. It abstracts many of the complexities of React Native development.

- Rapid Development: Expo provides a streamlined development workflow, making it easier for developers to get started and quickly build mobile apps without the need for native code expertise or complex setup.

- Abstraction of Native Code: While Expo provides access to a wide range of native device features, it abstracts the need for writing custom native code, which can be a limitation for apps that require extensive native customization.

- Managed and Bare Workflow: Expo offers both a "Managed" workflow (where Expo takes care of much of the build process) and a "Bare" workflow (where developers have more control and can add custom native modules).


### [expo snack](https://snack.expo.io/)


## 1. Checkout this tool. What does snack allow you to do?

Expo Snack enables developers to create, test, and share React Native apps in a web-based environment, eliminating the need for local setup and facilitating rapid prototyping and collaboration. It provides an instant mobile development playground with access to Expo's libraries and real device testing.



### [ejecting](https://docs.expo.io/versions/latest/expokit/eject)



## 1. What does “eject” mean within the context of Expo?

In the context of Expo, "eject" refers to the process of transitioning from the standard Expo development environment to a more customizable and full-featured setup. When you "eject" from Expo, you have two options:

- Eject to Bare Workflow: This option allows you to move into the "bare" workflow, where you have full control over your native Android and iOS projects. While you can still use Expo APIs, you also gain the ability to customize your native code and configurations.

- Eject to ExpoKit (deprecated): This option provided native projects along with ExpoKit, an Objective-C and Java library that allowed you to use the Expo SDK and platform as part of a larger standard native project. However, support for ExpoKit was removed after SDK 38.


## 2. When should you not eject?


You should consider not ejecting from Expo when you prioritize rapid development, lack native development expertise, have limited customization needs that Expo can fulfill, or aim for cross-platform compatibility. Staying in the managed Expo workflow simplifies development, reduces complexity, and is ideal for smaller to medium-sized apps or projects with resource constraints. You can always choose to eject later if your project requirements change.


## 3. Why might you choose to eject?


You might choose to eject from Expo when you need extensive customization, access to native modules or platform-specific features, or improved performance optimization. Ejecting provides full control over native code and configurations, enabling advanced development and fine-tuning for specific project requirements.



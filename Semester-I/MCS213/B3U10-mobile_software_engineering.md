<!-- TOC start (generated with https://github.com/derlin/bitdowntoc) -->

- [MOBILE SOFTWARE ENGINEERING](#mobile-software-engineering)
  - [Transition from Design to Coding of Mobile Applications](#transition-from-design-to-coding-of-mobile-applications)
    - [Creating a Transition](#creating-a-transition)
    - [Transition Using Wireframes](#transition-using-wireframes)
    - [Prototyping Mobile UI Animations](#prototyping-mobile-ui-animations)
    - [Application Wireframing Features](#application-wireframing-features)
    - [Importance of UI/UX](#importance-of-uiux)
    - [Animated Transitions](#animated-transitions)
    - [Transition Framework Features](#transition-framework-features)
    - [Basic Process to Animate Between Layouts](#basic-process-to-animate-between-layouts)
  - [Scenes in Android](#scenes-in-android)
  - [Overview](#overview)
  - [Creating Scenes](#creating-scenes)
    - [From Layout Resource File](#from-layout-resource-file)
    - [Define Layouts for Scenes](#define-layouts-for-scenes)
    - [Generate Scenes from Layouts](#generate-scenes-from-layouts)
    - [Create a Scene in Your Code](#create-a-scene-in-your-code)
    - [Create Scene Actions](#create-scene-actions)
  - [Apply a Transition](#apply-a-transition)
    - [Transition Lifecycle](#transition-lifecycle)
    - [Supported Transitions](#supported-transitions)
  - [Using Android Wireframes Effectively](#using-android-wireframes-effectively)
  - [Benefits of Using Wireframes](#benefits-of-using-wireframes)
  - [Elements of Mobile Applications](#elements-of-mobile-applications)
    - [1. Product Strategy](#1-product-strategy)
    - [2. Understanding Application Needs](#2-understanding-application-needs)
    - [3. User Interface Design (UI)](#3-user-interface-design-ui)
    - [4. Screen Resolution](#4-screen-resolution)
    - [5. Graphics](#5-graphics)
    - [6. User Experience Design (UX)](#6-user-experience-design-ux)
    - [7. Performance (Speed)](#7-performance-speed)
    - [8. User-Friendly Navigation](#8-user-friendly-navigation)
    - [9. Application Content](#9-application-content)
    - [10. Mobile Device Performance](#10-mobile-device-performance)
    - [11. Social Sharing Option](#11-social-sharing-option)
    - [12. Security](#12-security)
    - [13. Power Consumption](#13-power-consumption)
    - [14. Compatibility](#14-compatibility)
    - [15. Simplicity](#15-simplicity)
    - [16. Offline Functionality](#16-offline-functionality)
    - [17. High Performance](#17-high-performance)
    - [18. Feedback Option](#18-feedback-option)
    - [19. Regular Updates](#19-regular-updates)
    - [20. Marketing](#20-marketing)
  - [Approaches to the Development of Mobile Applications](#approaches-to-the-development-of-mobile-applications)
    - [Types of Mobile Development Approaches](#types-of-mobile-development-approaches)
    - [Choosing the Right Approach](#choosing-the-right-approach)
    - [Native Application Development](#native-application-development)
      - [Prime Reasons to Choose Native Mobile App Development](#prime-reasons-to-choose-native-mobile-app-development)
      - [Advantages of Native Application Development](#advantages-of-native-application-development)
    - [Native iOS Application Development Stack](#native-ios-application-development-stack)
      - [Objective-C](#objective-c)
      - [Swift](#swift)
    - [Toolset: AppCode and Xcode](#toolset-appcode-and-xcode)
      - [AppCode](#appcode)
      - [Xcode](#xcode)
    - [Android Application Development Stack](#android-application-development-stack)
      - [Kotlin](#kotlin)
      - [Java](#java)
    - [Toolset: Android Studio and Eclipse](#toolset-android-studio-and-eclipse)
      - [Eclipse](#eclipse)
      - [Android Studio](#android-studio)
    - [Cross-Platform Application Development](#cross-platform-application-development)
    - [Hybrid Application Development](#hybrid-application-development)
    - [Rapid Mobile Application Development (RMAD)](#rapid-mobile-application-development-rmad)
    - [Progressive Web Applications (PWAs)](#progressive-web-applications-pwas)
  - [Check Your Progress-1](#check-your-progress-1)
  - [Check Your Progress-2](#check-your-progress-2)
  - [Check Your Progress-3](#check-your-progress-3)

<!-- TOC end -->

<!-- TOC --><a name="mobile-software-engineering"></a>
# MOBILE SOFTWARE ENGINEERING

<!-- TOC --><a name="transition-from-design-to-coding-of-mobile-applications"></a>
## Transition from Design to Coding of Mobile Applications

***Transition***
    - **Definition:** Manages animations during scene changes.
    - **Main Jobs:** 
    1. Capture property values.
    2. Play animations based on changes to captured property values.
    - **Custom Transition:** 
    - Knows relevant property values on view objects.
    - Animates changes to those values.

<!-- TOC --><a name="creating-a-transition"></a>
### Creating a Transition
- Define starting and ending scenes.
- Create a `Transition` object for animation.
- Use built-in transitions either via resource file or directly in code.

<!-- TOC --><a name="transition-using-wireframes"></a>
### Transition Using Wireframes
- **Purpose:** Demonstrate functionalities, user interactions, and screen flows.
- **Benefit:** Minimizes upfront development effort and cost.
- **Android Wireframes:** Screen sketches to present and explain design ideas to customers.
- **Goal:** Reach consensus on design transitioning into proposed application.

<!-- TOC --><a name="prototyping-mobile-ui-animations"></a>
### Prototyping Mobile UI Animations
- **Purpose:** Guide users through the mobile application experience.
- **Key Points:**
  - Animations should be relevant and purposeful.
  - Enhance user experience and conversion goals.
  - Include effects like sliding, flipping, turning, popping, fading, folding, dropping, bouncing.

<!-- TOC --><a name="application-wireframing-features"></a>
### Application Wireframing Features
- **Benefits:**
  - Speed up the wireframing process.
  - Get real feedback from user testing.
  - Accelerate innovation and avoid rework.
  - Launch the right app.

<!-- TOC --><a name="importance-of-uiux"></a>
### Importance of UI/UX
- **Critical for Success:**
  - Exceptional UI/UX needed alongside perfect backend code.
  - UI/UX and visuals can make apps an instant hit or cause them to be ignored.
- **UI vs. UX:**
  - **UI (User Interface):** Visuals and graphics.
  - **UX (User Experience):** User retention and experience.
  - UI is a subset of UX.
  
<!-- TOC --><a name="animated-transitions"></a>
### Animated Transitions
- **Impact:** Difference between a great app and a mediocre one.
- **Role:** 
  - Make UI elements visible/invisible.
  - Contribute to a seamless user experience.

<!-- TOC --><a name="transition-framework-features"></a>
### Transition Framework Features
- **Animate Layout Changes:**
  - Provide starting and ending layout.
  - Choose animation type (e.g., fade, change view sizes).
- **Group-level Animations:** Apply effects to all views in a hierarchy.
- **Built-in Animations:** Use predefined effects (e.g., fade out, movement).
- **Resource File Support:** Load hierarchies and animations from layout resource files.
- **Lifecycle Callbacks:** Control over animation and hierarchy changes.

<!-- TOC --><a name="basic-process-to-animate-between-layouts"></a>
### Basic Process to Animate Between Layouts
1. Create a `Scene` object for starting and ending layouts.
   - Starting layout often determined automatically.
2. Create a `Transition` object to define the animation type.
3. Call `TransitionManager.go()`.
4. System runs the animation to swap layouts.

![Basic illustration of how the transition framework creates an animation](images/transition-framework.png)

<!-- TOC --><a name="scenes-in-android"></a>
## Scenes in Android

<!-- TOC --><a name="overview"></a>
## Overview
- **Scenes**: Store the state of a view hierarchy, including all its views and property values.
- **Transitions Framework**: Runs animations between a starting and an ending scene.

<!-- TOC --><a name="creating-scenes"></a>
## Creating Scenes
<!-- TOC --><a name="from-layout-resource-file"></a>
### From Layout Resource File
- **Usage**: Suitable for static view hierarchies.
- **Process**:
  - Retrieve the scene root as a `ViewGroup` instance.
  - Use `Scene.getSceneForLayout()` with the scene root and the layout file resource ID.

<!-- TOC --><a name="define-layouts-for-scenes"></a>
### Define Layouts for Scenes
- **Example Layouts**:
  - Main layout with a text label and a child layout.
  - First scene: Relative layout with two text fields.
  - Second scene: Relative layout with the same two text fields in a different order.
- **Note**: Animation occurs within the child layout; the text label in the main layout remains static.

<!-- TOC --><a name="generate-scenes-from-layouts"></a>
### Generate Scenes from Layouts
- Obtain a scene for each layout using the scene root and layout resource ID.

<!-- TOC --><a name="create-a-scene-in-your-code"></a>
### Create a Scene in Your Code
- **Usage**: Modify view hierarchies directly in code or generate them dynamically.
- **Process**: Use the `Scene(sceneRoot, viewHierarchy)` constructor.

<!-- TOC --><a name="create-scene-actions"></a>
### Create Scene Actions
- **Custom Scene Actions**: Define custom actions to run when entering or exiting a scene.
  - **Use Cases**:
    - Animate views not in the same hierarchy.
    - Animate views the transitions framework cannot animate automatically.
  - **Implementation**: Define actions as `Runnable` objects and pass them to `Scene.setExitAction()` or `Scene.setEnterAction()`.

<!-- TOC --><a name="apply-a-transition"></a>
## Apply a Transition
- **Transition Object**: Represents the style of animation between scenes.
  - **Built-in Subclasses**: `AutoTransition`, `Fade`, etc.
  - **Process**: Run animation between scenes using `TransitionManager.go(endScene, transition)`.

<!-- TOC --><a name="transition-lifecycle"></a>
### Transition Lifecycle
- **Enter Transition**: Determines how views enter the scene.
- **Exit Transition**: Determines how views exit the scene.
- **Shared Elements Transition**: Determines how shared views transition between activities.

<!-- TOC --><a name="supported-transitions"></a>
### Supported Transitions
- **Enter and Exit Transitions**:
  - `explode`: Moves views in or out from the center.
  - `slide`: Moves views in or out from one of the edges.
  - `fade`: Changes the opacity of a view.
- **Shared Elements Transitions**:
  - `changeBounds`: Animates layout bounds changes.
  - `changeClipBounds`: Animates clip bounds changes.
  - `changeTransform`: Animates scale and rotation changes.
  - `changeImageTransform`: Animates size and scale changes.

<!-- TOC --><a name="using-android-wireframes-effectively"></a>
## Using Android Wireframes Effectively
- **Purpose**: Clarify user interface, consider usability early, engage clients, cost-efficient.
- **Tips**:
  - Keep wireframes simple and quick to produce.
  - Use placeholders or dummy text to avoid distractions.
  - Annotate elements and behaviors only when necessary.
- **Tools**:
  - **State**: Create child wireframes based on an existing one.
  - **Storyboard**: Present screen flow of a scenario.
  - **User Story Management**: Record user concerns and requirements, include wireframes in scenarios.

<!-- TOC --><a name="benefits-of-using-wireframes"></a>
## Benefits of Using Wireframes
1. Clarify user interface.
2. Early consideration of usability.
3. Engaged clients.
4. Cost-efficient: Easy to create, edit, and inexpensive for basic screen sketches.


<!-- TOC --><a name="elements-of-mobile-applications"></a>
## Elements of Mobile Applications

<!-- TOC --><a name="1-product-strategy"></a>
### 1. Product Strategy
- Essential for aligning business goals with application development.
- Prioritize features that bring measurable business value.

<!-- TOC --><a name="2-understanding-application-needs"></a>
### 2. Understanding Application Needs
- Define the scope clearly based on business priorities.
- Ensure the application addresses critical aspects of the business.

<!-- TOC --><a name="3-user-interface-design-ui"></a>
### 3. User Interface Design (UI)
- Focus on usability and intuitive design.
- Design UI to enhance user experience (UX).

<!-- TOC --><a name="4-screen-resolution"></a>
### 4. Screen Resolution
- Consider different device screen sizes and resolutions.
- Adhere to technical guidelines for optimal display.

<!-- TOC --><a name="5-graphics"></a>
### 5. Graphics
- Importance of appealing visuals for user engagement.
- Ensure compatibility across various screen sizes.

<!-- TOC --><a name="6-user-experience-design-ux"></a>
### 6. User Experience Design (UX)
- Create positive interactions and emotional connections.
- Design intuitive and interactive features.

<!-- TOC --><a name="7-performance-speed"></a>
### 7. Performance (Speed)
- Optimize application speed to enhance user satisfaction.
- Ensure minimal loading times and smooth operation.

<!-- TOC --><a name="8-user-friendly-navigation"></a>
### 8. User-Friendly Navigation
- Simplify navigation for ease of use.
- Avoid complex interfaces to improve usability.

<!-- TOC --><a name="9-application-content"></a>
### 9. Application Content
- Provide clear and concise information.
- Avoid keyword stuffing and focus on relevance.

<!-- TOC --><a name="10-mobile-device-performance"></a>
### 10. Mobile Device Performance
- Optimize application size to conserve device resources.
- Minimize battery and processor usage for efficient operation.

<!-- TOC --><a name="11-social-sharing-option"></a>
### 11. Social Sharing Option
- Integrate social media sharing for user engagement.
- Leverage social sharing to increase application visibility.

<!-- TOC --><a name="12-security"></a>
### 12. Security
- Prioritize user data protection and application security.
- Implement robust encryption and secure protocols.

<!-- TOC --><a name="13-power-consumption"></a>
### 13. Power Consumption
- Optimize app resources to conserve battery life.
- Minimize background processes that drain power.

<!-- TOC --><a name="14-compatibility"></a>
### 14. Compatibility
- Ensure compatibility with different OS versions.
- Update features to match platform advancements.

<!-- TOC --><a name="15-simplicity"></a>
### 15. Simplicity
- Emphasize simplicity in design and functionality.
- Improve user adoption with intuitive interfaces.

<!-- TOC --><a name="16-offline-functionality"></a>
### 16. Offline Functionality
- Enable offline access to enhance usability.
- Cater to users in areas with limited connectivity.

<!-- TOC --><a name="17-high-performance"></a>
### 17. High Performance
- Ensure consistent and reliable application performance.
- Address performance issues promptly to retain users.

<!-- TOC --><a name="18-feedback-option"></a>
### 18. Feedback Option
- Provide channels for user feedback and reviews.
- Use feedback to improve application features.

<!-- TOC --><a name="19-regular-updates"></a>
### 19. Regular Updates
- Release updates to add new features and enhancements.
- Maintain application relevance and user engagement.

<!-- TOC --><a name="20-marketing"></a>
### 20. Marketing
- Implement effective marketing strategies to promote the app.
- Increase visibility and attract a broader audience.

<!-- TOC --><a name="approaches-to-the-development-of-mobile-applications"></a>
## Approaches to the Development of Mobile Applications

<!-- TOC --><a name="types-of-mobile-development-approaches"></a>
### Types of Mobile Development Approaches
1. Native Application Development
2. Cross-Platform Application Development
3. Hybrid Application Development
4. Rapid Mobile Application Development (RMAD)
5. Progressive Web Applications (PWAs)

<!-- TOC --><a name="choosing-the-right-approach"></a>
### Choosing the Right Approach
- Define the purpose of the mobile application based on target audience needs.
- Estimate project timeline, financial, and technical resources.
- Choose the most favorable development approach.

<!-- TOC --><a name="native-application-development"></a>
### Native Application Development
- **Definition:** Uses platform-specific programming languages, SDKs, and development environments.
- **Features:** Developed separately for each platform with different technology stacks.
- **Benefits:** Higher performance and responsiveness, supports all platform features.

<!-- TOC --><a name="prime-reasons-to-choose-native-mobile-app-development"></a>
#### Prime Reasons to Choose Native Mobile App Development
1. Access to Complete Device Features
2. Scalability
3. Offline Performance
4. Stability
5. Cost

<!-- TOC --><a name="advantages-of-native-application-development"></a>
#### Advantages of Native Application Development
- Best performance
- Platform-specific UI implementation
- 100% support of OS features
- Total access to hardware-related features
- Clear application update path and supported toolset
- Highly reliable, secure, and responsive

<!-- TOC --><a name="native-ios-application-development-stack"></a>
### Native iOS Application Development Stack
- **Programming Languages:** Objective-C and Swift

<!-- TOC --><a name="objective-c"></a>
#### Objective-C
- High-level, object-oriented language modeled like C.
- Used for complex projects and software engineering challenges.
- **Advantages:**
  - Works with C++
  - Well-tested and recommended
  - Expressive message syntax
  - Simple and effective use of private APIs
  - Multiple third-party libraries
  - Large community support

<!-- TOC --><a name="swift"></a>
#### Swift
- Multi-purpose and multi-paradigm language.
- **Advantages:**
  - Open-source
  - Code less prone to error
  - Dynamic libraries
  - Simplifies development and maintenance
  - Enhances code reusability and readability
  - Multi-feature, fast, and compatible with Objective-C
  - Supports Cocoa Touch frameworks and Apple’s Cocoa
  - Multi-device support
  - Community support

<!-- TOC --><a name="toolset-appcode-and-xcode"></a>
### Toolset: AppCode and Xcode

<!-- TOC --><a name="appcode"></a>
#### AppCode
- Fast coding alternative to Xcode.
- Supports multiple programming languages.
- Drawback: Can only design interfaces with written code.

<!-- TOC --><a name="xcode"></a>
#### Xcode
- Official IDE of Apple.
- Supports mobile and desktop application development.
- Features: User interface development, gaming applications, Git repositories, documentation, debugging tools, graphical editor.
- Supports multiple programming languages.

<!-- TOC --><a name="android-application-development-stack"></a>
### Android Application Development Stack
- **Programming Languages:** Java and Kotlin

<!-- TOC --><a name="kotlin"></a>
#### Kotlin
- Recent, object-oriented, open-source language.
- Interoperable with Java.
- **Advantages:**
  - Runs on multi-platform
  - Concise and secure code
  - Supports higher-order functions
  - Big community support
  - Easy code maintenance

<!-- TOC --><a name="java"></a>
#### Java
- Widely used class-based, object-oriented language.
- Ideal for mobile and web applications, Big Data.
- **Advantages:**
  - Highly secure
  - Great network capability
  - Portable and scalable code
  - Automatic memory management
  - Robust and easy to compile
  - Rich open-source tools and libraries

<!-- TOC --><a name="toolset-android-studio-and-eclipse"></a>
### Toolset: Android Studio and Eclipse

<!-- TOC --><a name="eclipse"></a>
#### Eclipse
- Free, open-source SDK.
- Originated from IBM, primarily coded in Java.
- Extendable with plug-ins.

<!-- TOC --><a name="android-studio"></a>
#### Android Studio
- Google’s integrated development environment.
- Features: Code editing, performance tooling, debugging, flexible development, immediate build/deploy system.
- Works with multiple PC operating systems.

<!-- TOC --><a name="cross-platform-application-development"></a>
### Cross-Platform Application Development
- **Definition:** Applications that can run on different platforms using languages and tools different from native toolsets.
- **Advantages:**
  - Uniformity across platforms
  - Effective budget control
  - Easy implementation
  - Simultaneous publishing
  - Reusable source code
  - High demographic coverage
  - Fast time to market

<!-- TOC --><a name="hybrid-application-development"></a>
### Hybrid Application Development
- **Definition:** Blend of native and web applications.
- **Features:** Developed using standard web technologies (JavaScript, CSS, HTML5) within a native shell.
- **Advantages:**
  - Single development team
  - Short time to market
  - Easy portability of code
  - Capable use of hardware components
  - Native-like user experience
  - Lower development cost
  - Works online and offline

<!-- TOC --><a name="rapid-mobile-application-development-rmad"></a>
### Rapid Mobile Application Development (RMAD)
- **Definition:** Develops cross-platform applications quickly using code-free or low-code tools.
- **Platforms:** Examples include Alpha Software, MobileFrame, MobileSmith.
- **Advantages:**
  - Secure
  - Works online and offline
  - Good backend data integration
  - Cross-platform support
  - Code-free development
  - Requires little developer experience
  - Reusable components
  - Low production cost

<!-- TOC --><a name="progressive-web-applications-pwas"></a>
### Progressive Web Applications (PWAs)
- **Definition:** Native app-like web applications using HTML.
- **Advantages:**
  - Easy application maintenance
  - Single codebase
  - Mobile-friendly UI
  - No need for application stores
  - Works online and offline

<!-- TOC --><a name="check-your-progress-1"></a>
## Check Your Progress-1
1. Transition holds _________ that will be run on its targets during a scene change. 

<!-- TOC --><a name="check-your-progress-2"></a>
## Check Your Progress-2
1. Write few elements of mobile application development?
2. What is user friendly navigation?

<!-- TOC --><a name="check-your-progress-3"></a>
## Check Your Progress-3
1. Which application development is the use of platform-specific programming languages?
2. Which approach can be used to run application the on different platforms?
3. Which application Development approach is used to develop cross-platform applications in a short time?
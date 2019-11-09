# Kotlin Native / Multiplatform FAQ

## What's Kotlin Native?

It's a technique to generate native code via LLVM. Think C/C++ compilers, but Kotlin! ♥️

## Nice! So is that a magical way to compile Java code / libs to native?

Unfortunately, no. But if you have a PDF lib in Java, and you have a similar lib on iOS, you can use Kotlin Multiplatform to define a common `expect fun createPdf()`, and create specific implementations with the keyword `actual`.

In addition, there is a way to create Multiplatform libs - and of course, to import those created by other developers! Check out TODO

## Is this a way to share code on Android/iOS?

Yes! And you can even share code for the web, too. Check out Kotlin/JS.

## How does this work for iOS?

It will generate a framework via a `gradlew` task. The framework contains the native code, along with a `.h` header file with ObjectiveC + Swift definitions. You can then include this framework into your Xcode project.

Also, you can setup your Xcode project to build that framework automatically on each build. Check out this really nice hands-on! TODO

## What is the recommended setup for iOS + Android devs to work together?

The best way is to check in both projects into a single Git repo. That's because then both projects depend naturally on the shared code. It's not recommended to check in the native framework into Git. You wouldn't do that with your CocoaPods / Maven / Gradle dependencies. 😉

## How can I create a CocoaPod library with Kotlin Native?

## How can I debug Kotlin Native?

## How does code completion work in Xcode?

## How to test all that?

## What happens if an exception is thrown in shared Kotlin code?

## How's the performance?

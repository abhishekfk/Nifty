# CwlUtils

A collection of utilities written as part of articles on [Cocoa with Love](https://cocoawithlove.com)

## Included functionality

The following features are included in the library.

* [CwlStackFrame.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlStackFrame.swift) from [Better stack traces in Swift](https://cocoawithlove.com/blog/2016/02/28/stack-traces-in-swift.html)
* [CwlSysctl.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlSysctl.swift) from [Gathering system information in Swift with sysctl](https://www.cocoawithlove.com/blog/2016/03/08/swift-wrapper-for-sysctl.html)
* [CwlUnanticipatedError.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlUnanticipatedError.swift) from [Presenting unanticipated errors to users](https://www.cocoawithlove.com/blog/2016/04/14/error-recovery-attempter.html)
* [CwlScalarScanner.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlScalarScanner.swift) from [Swift name demangling: C++ vs Swift for parsing](https://www.cocoawithlove.com/blog/2016/05/01/swift-name-demangling.html)
* [CwlRandom.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlRandom.swift) from [Random number generators in Swift](https://www.cocoawithlove.com/blog/2016/05/19/random-numbers.html)
* [CwlMutex.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlMutex.swift) from [Mutexes and closure capture in Swift](https://www.cocoawithlove.com/blog/2016/06/02/threads-and-mutexes.html)
* [CwlDispatch.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlDispatch.swift) from [Design patterns for safe timer usage](https://www.cocoawithlove.com/blog/2016/07/30/timer-problems.html)
* [CwlResult.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlResult.swift) from [Values and errors, part 1: 'Result' in Swift](https://www.cocoawithlove.com/blog/2016/08/21/result-types-part-one.html)
* [CwlDeque.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlDeque.swift) from [Optimizing a copy-on-write double-ended queue in Swift](https://www.cocoawithlove.com/blog/2016/09/22/deque.html)
* [CwlExec.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlExec.swift) from [Specifying function execution contexts](https://www.cocoawithlove.com/blog/specifying-execution-contexts.html)
* [CwlDebugContext.swift](https://github.com/mattgallagher/CwlUtils/blob/master/Sources/CwlUtils/CwlDebugContext.swift) from [Testing actions over time](https://www.cocoawithlove.com/blog/testing-actions-over-time.html)

## Adding to your project

This project can be used by manual inclusion in your projects or through any of the Swift Package Manager, CocoaPods or Carthage.

Minimum requirements are iOS 8 (simulator-only) or macOS 10.10.

### Manual inclusion

1. In a subdirectory of your project's directory, run `git clone https://github.com/mattgallagher/CwlUtils.git`
2. Drag the "CwlUtils.xcodeproj" file from the Finder into your own project's file tree in Xcode
3. Add the "CwlUtils.framework" from the "Products" folder of the CwlUtils project's file tree to the "Copy Files (Frameworks)" build phases of any target that you want to include this module.

That third step is a little tricky if you're unfamiliar with Xcode but it involves:

1. click on your project in the file tree
2. click on the target to whih you want to add this module
3. select the "Build Phases" tab
4. if you don't already have a "Copy File" build phase with a "Destination: Frameworks", add one using the "+" button in the top left of the tab
5. click the "+" within the "Copy File (Frameworks)" phase and from the list that appears, select the "CwlUtils.framework" (if there are multiple frameworks with the same name, look for the one that appears *above* the corresponding macOS or iOS CwlUtils testing target).

### Swift Package Manager

Add the following to the `dependencies` array in your "Package.swift" file:

    .Package(url: "https://github.com/mattgallagher/CwlUtils.git", majorVersion: 1),

Or, if you're using the `swift-tools-version:4.0` package manager, add the following to the `dependencies` array in your "Package.swift" file:

    .package(url: "https://github.com/mattgallagher/CwlUtils.git", majorVersion: 1)

### CocoaPods

Add the following to your target in your "Podfile":

    pod 'CwlUtils', :git => 'https://github.com/mattgallagher/CwlUtils.git'

### Carthage

Add the following line to your Cartfile:

    git "https://github.com/mattgallagher/CwlUtils.git" "master"

# CQMLBind

[libqmlbind](https://github.com/seanchas116/libqmlbind) wrapper for Swift

## Usage

CQMLBind requires Swift package manager.

### Add as dependency in your Package.swift

First, add CQMLBind as a dependency package in your `Package.swift` file.

```swift
import PackageDescription

let package = Package(
    dependencies: [
        .Package(url: "https://github.com/seanchas116/CQMLBind.git", Version(0,0,1))
    ]
)
```

### Build libqmlbind itself

Then, build [libqmlbind](https://github.com/seanchas116/libqmlbind) itself.
(instructions are written in libqmlbind readme)

### Build your package

To build your package which uses CQMLBind, pass libqmlbind paths to compile and link successfully.

```
swift build -Xcc -I/path/to/libqmlbind/qmlbind/include -Xlinker -L/path/to/libqmlbind/qmlbind/ -Xlinker -rpath -Xlinker /path/to/libqmlbind/qmlbind/
```

# CQMLBind

[libqmlbind](https://github.com/seanchas116/libqmlbind) wrapper for Swift

## Usage

CQMLBind requires Swift package manager.

### Install libqmlbind

```
> brew tap seanchas116/libqmlbind
> brew install libqmlbind
```

### Add as dependency in your Package.swift

In your `Package.swift` file:

```swift
import PackageDescription

let package = Package(
    dependencies: [
        .Package(url: "https://github.com/seanchas116/CQMLBind.git", Version(0,0,1))
    ]
)
```

### Build your package

```
swift build -Xcc -I/usr/local/include -Xlinker -L/usr/local/lib -Xlinker -rpath -Xlinker /usr/local/lib
```

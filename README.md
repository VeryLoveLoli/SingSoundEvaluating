# SingSoundEvaluating

先声教育声音评测 SingSound 0.6.3 SDK XCFramework SwiftPackage

### bundle

`SingSound.Bundle` 直接添加到主项目，放在 `SwiftPackage` 会包含在默认的 `bundle` 下

### libs

`libssound.a` 没有头文件，无法加入 `Framework` 合成 `XCFramework`，直接添加到主项目

### 工程引用
在 `Link Binary With Libraries` 添加 `libz.tbd`

### SwiftPackage 引用

```swift
.target(
    name: "Name",
    dependencies: ["SingSoundEvaluating"],
    linkerSettings: [.linkedLibrary("z")]),
```

# 引用 Library 项目

引用 Library 项目与引用其他项目一样：

``` Groovy
dependencies {
    compile project(':libraries:lib1')
    compile project(':libraries:lib2')
}
```

___

> 注意: 如果要引用多个 Library，那么引用的先后顺序将非常重要。这类似于旧的构建系统的 `project.properties` 文件中的依赖顺序。

___

# 多项目报告

在一个配置了多个应用项目和多个 Library 项目的多项目里，当同时运行所有测试的时候，只生成一个记录了所有测试报告的文件可能是非常有用的。

为了实现这个目的，需要在同一个依赖文件（<font color='red'>译注：</font>指的是使用 android gradle 插件的依赖文件）中添加另一个插件。可以通过以下方式添加：

```  Groovy
buildscript {
    repositories {
        mavenCentral()
    }

    dependencies {
        classpath 'com.android.tools.build:gradle:0.5.6'
    }
}

apply plugin: 'android-reporting'
```

必须添加在项目的根目录下，例如，与 *settings.gradle* 文件同级目录的 *build.gradle* 文件中。

之后，在命令行中进入项目根目录，输入以下命令就可以运行所有测试并合并所有报告：

``` sh
gradle deviceCheck mergeAndroidReports --continue
```

---

> 注意：这里的 `--continue` 选项将允许所有测试，即使子项目中的任何一个测试运行失败都不会停止。如果没有这个选项，其中一个测试失败则会终止所有测试的运行，此时部分项目可能还未执行测试。

---
# 插件依赖

一个插件也许会依赖其他插件的类，可能是绑定的，第三方的，或是同一个作者的。这个文档描述了定义插件依赖和可选插件依赖的语法。想要得到更多有关IntelliJ平台模块依赖的内容，请见这份文档的Part Ⅱ：[IntelliJ平台产品的插件兼容性](plugin_compatibility.md)

> **注** 无法指定依赖插件的最大或最小版本.

为了描述对其他插件或模块的类的依赖，必须执行以下三个步骤：

### 1.准备沙盒

如果插件没有被目标IDE绑定，运行你的目标IDE的实例（沙盒）并安装插件。

### 2.项目启动

> **注** 插件可访问的属性请参考[gradle插件:配置](gradle_plugin_configuration.md)

如果项目使用Groovy的Gradle脚本构建插件，添加依赖到buile.gradle文件中的，IntelliJ块`plugins`参数，例：

```groovy
intellij{
	plugins 'org.jetbrains.kotlin:1.3.11-release-IJ2018.3-1'
}
```

如果项目使用Kotlin风格的Gradle构建脚本，在intellij块中使用`setPlugins()`，例：

```kotlin
intellij {
        setPlugins("org.jetbrains.kotlin:1.3.11-release-IJ2018.3-1")
}
```


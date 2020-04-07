# 插件内容

插件的jar文件必须包含：

- 配置文件(META-INF/plugin.xml)]([配置文件](plugin_configuration_file.md))
- 实现插件功能的类
- 推荐：插件的logo文件(META-INF/pluginIcon*.svg)([插件logo](plugin_logo.md))

### 没有依赖的插件

一个由单独jar文件组成的插件，是放在/plugins目录下。

```
.IntelliJIDEAx0/
└── plugins
    └── sample.jar
        ├── com/foo/...
        │   ...
        │   ...
        └── META-INF
            ├── plugin.xml
            ├── pluginIcon.svg
            └── pluginIcon_dark.svg
```

### 有依赖的插件

插件的jar文件与其需要捆绑的库，一起被放在插件根目录的/lib路径下。

所有/lib路径下的jar文件自动添加到classpath（详见[插件的Class Loaders](plugin_class_loader.md))

```
   .IntelliJIDEAx0/
   └── plugins
       └── sample
           └── lib
               ├── lib_foo.jar
               ├── lib_bar.jar
               │   ...
               │   ...
               └── sample.jar
                   ├── com/foo/...
                   │   ...
                   │   ...
                   └── META-INF
                       ├── plugin.xml
                       ├── pluginIcon.svg
                       └── pluginIcon_dark.svg
```
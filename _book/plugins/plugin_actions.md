# 插件Actions

IntelliJ平台提供了actions的概念。一个action是一个类，派生自`AcAction`类，它的`actionPerformed()`方法当菜单项或工具栏按钮被选中时调用。

Actions是一个用户调用你插件功能的最常用的方法。一个Action可以从一个菜单或工具栏，快捷键或通过Find Action接口来调用。

Actions被组织成组，组又可以被其他组包含。一个Action的组可以形成一个工具栏或一个菜单。组的子组可以形成菜单的子菜单。你可以查看详细信息，来了解如何创建和注册你的action在[IntelliJ平台Action系统](action_system.md)


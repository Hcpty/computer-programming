# Factory

需求：用戶只需要修改一行代碼，就能夠切換產品系列。

方案：引入Factory，由Factory返回產品。

案例：

```Java
WidgetFactory widgetFactory = new PMWidgetFactory();
Window window = widgetFactory.createWindow();
ScrollBar scrollBar = widgetFactory.createScrollBar();
```

用戶只需要把第一行代碼修改成如下，就能夠將部件系列從Presentation Manager切換到Motif：

```Java
WidgetFactory widgetFactory = new MotifWidgetFactory();
```

Factory返回產品的操作稱爲Factory Method。

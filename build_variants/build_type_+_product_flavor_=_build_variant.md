# 构建类型+产品定制=构建变种版本

正如前面章节所提到的，每一个 *Build Type* 都会生成一个新的 APK。

*Product Flavors* 同样也会做这些事情：项目的输出将会拼接所有可能的 *Build Types* 和 *Product Flavors*（如果有定义 Flavor）的组合。

每一种组合（包含 *Build Type* 和 *Product Flavor*）就是一个 *Build Variant*（构建变种版本）。

例如，在之前的 Flavor 声明例子中与默认的 **<font color='green'>debug</font>** 和 **<font color='green'>release</font>** 两个 *Build Types*  将会生成4个 *Build Variants*：

* Flavor1 - debug
* Flavor1 - release
* Flavor2 - debug
* Flavor2 - release

项目中如果没有定义 flavor 同样也会有 *Build Variants*，只是使用的是 **<font color='green'>default</font>** （默认）的 flavor/config， 同时默认的是没有名字的，所以生成的 build variant 列表看起来就跟 *Build Type* 列表一样。
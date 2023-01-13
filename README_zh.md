# Tangnano9k入门

可选择如下语言
[:uk:](README.md) [:cn:](README_zh.md)

最近我准备学fpga，买了Sipeed的[Tangnano9k](https://wiki.sipeed.com/hardware/zh/tang/Tang-Nano-9K/Nano-9K.html)开发板，虽然我也准备了一块Zynq的板子做正式点地学习，但是Xilinx必须让我装它一堆乱七八糟的IDE，以至于我没法在我的Macbook上顺利跑起来
（我已经做到docker跑vivado到生成bitstream文件了，最后openFPGALoader实在装不进去）。Sipeed的这块板子官方给的文档都是用高云的IDE，还要整什么「Licence」这种人神共愤的设计，不过我们可爱的Github上有完全绕开它的开源工具链，这就让人老脸一红美滋滋了。

写这个文档主要是为了给别的买了板子不知道做什么的萌新们一个傻瓜式的入门，也为了整理自己的学习过程，给一个系统化的认知过程。我毕竟是学数学出身的，写这个教程肯定会搞点什么惨绝人寰的错误，届时希望各位大佬不吝赐教。

这个教程可能就涵盖了一丁点的Verilog教程，我认为这种语法奇葩的玩意儿就应该用作编译器后端，当然我们这里也没有这么高大尚，简单点，用[Python](https://www.python.org)写一个代码生成器。所以希望大家能搞懂我用python做代码生成器点思路，然后各显神通整出自己喜爱的语言的版本。考量到受众的情况，可能python作元语言(meta-language)去生成verilog(target language)最适合教学，当然我认为coq(以及其类种种)这种神器才是最终归宿，有机会再整个活儿吧。因此我不会写什么testbench文件，仿真可以在python的模型中做，我会本着[SICP](https://mitpress.mit.edu/9780262510875/)的精神给出每一个步骤的行为描述，切记读懂思路亲自书写，不要翻译python代码。

## 准备环境

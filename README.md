# LoongsonCsprj2017
Computer System Project for Loongson FPGA Board in 2017

本仓库维护了一个计算机系统综合实验参考实现，内容包括所有的实验参考代码和文档。这个实现的目标如下。

1. 实现一个可运行龙芯FPGA实验板上的MIPS32S CPU（也可以直接使用龙芯的开源MIPS32 CPU），并支持串口、键盘、鼠标、VGA等简单外设；
2. 移植教学操作系统ucore到MIPS32S CPU上；
3. 移植Linux操作系统到MIPS32S CPU上；
3. 在ubuntu 16.04上实现一个交叉编译器，可以把符合decaf或C0的应用程序编译成MIPS32S上的应用程序，并在ucore或Linux上运行；
4. 进行其他可能的功能扩展。如，支持网络和调试工具等。

## 文档

先有一个文档描述板子的硬件信息；然后有一个文档描述FPGA上实现的CPU和I/O设备，并定义FPGA对上提供的接口信息；第三个文档描述在这个FPGA硬件实现基础上操作系统实现和系统调用接口；最后一个文档是编译器的实现和编译器与操作系统间关于系统库和系统调用的接口。

所有文档都放在doc目录下，各部分内容分别放在单独的文件中或指向相关文档的链接。

### 龙芯FPGA实验板的硬件信息

* [大赛实验箱介绍](/doc/大赛实验箱介绍_v1.00.pdf)

### 龙芯的开源MIPS32 CPU信息

* [soc_lite和soc_up介绍](/doc/soc_lite和soc_up介绍_v0.01.pdf)

### MIPS32S CPU及外设的参考实现

* [Jia Kai的MIPS32S CPU实现](https://git.net9.org/armcpu-devteam/armcpu)
* [Jia Kai实验报告](/doc/jiakai_report.pdf)

### 龙芯FPGA实验板上的ucore参考实现

* [ucore-thumips](https://github.com/z4yx/ucore-thumips/tree/for-ls232-soc_up)（`for-ls232-soc_up`分支已在龙芯开源CPU上验证）
* [ucore对于指令集及特权资源的说明](/doc/ucore_thumips.pdf)
* [硬件需求分析](/doc/ucore_requirements.pdf)

### 龙芯FPGA实验板上的Linux参考实现

### decaf交叉编译器参考实现

### C0交叉编译器参考实现

### 与实验相关的其他问题和解决建议



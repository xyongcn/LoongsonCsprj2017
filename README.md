# LoongsonCsprj2017
Computer System Project for Loongson FPGA Board in 2017

本仓库维护了一个计算机系统综合实验参考实现，内容包括所有的实验参考代码和文档。这个实现的目标如下。

1. 实现一个可运行龙芯FPGA实验板上的MIPS32S CPU（也可以直接使用龙芯的开源MIPS32 CPU），并支持串口、键盘、鼠标、VGA等简单外设；
2. 移植教学操作系统ucore到MIPS32S CPU上；
3. 移植Linux操作系统到MIPS32S CPU上；
3. 在ubuntu 16.04上实现一个交叉编译器，可以把符合decaf或C0的应用程序编译成MIPS32S上的应用程序，并在ucore或Linux上运行；
4. 进行其他可能的功能扩展。如，支持网络和调试工具等。

## 相关链接
 * [Wiki page](http://os.cs.tsinghua.edu.cn/oscourse/project/LoongsonCsprj2017)

## 文档

先有一个文档描述板子的硬件信息；然后有一个文档描述FPGA上实现的CPU和I/O设备，并定义FPGA对上提供的接口信息；第三个文档描述在这个FPGA硬件实现基础上操作系统实现和系统调用接口；最后一个文档是编译器的实现和编译器与操作系统间关于系统库和系统调用的接口。

所有文档都放在doc目录下，各部分内容分别放在单独的文件中或指向相关文档的链接。

### 龙芯FPGA实验板的硬件信息

* [大赛实验箱介绍](/doc/大赛实验箱介绍_v1.00.pdf)
* [龙芯FPGA开发板原理图](http://os.cs.tsinghua.edu.cn/oscourse/project/LoongsonCsprj2017#A20171011-FPGA-A7-PRJ-UDB_V1.1.pdf)

### 龙芯的开源MIPS32 CPU信息

* [soc_lite和soc_up介绍](/doc/soc_lite和soc_up介绍_v0.01.pdf)：这里介绍的是龙芯开源的两个经剪裁的MIPS32 CPU型号，soc_lite不带TLB，soc_up带TLB；
* [soc_demo代码](http://os.cs.tsinghua.edu.cn/oscourse/project/LoongsonCsprj2017?action=AttachFile&do=view&target=soc_demo_v0.02.tar.xz)

### MIPS32S CPU及外设的参考实现

* [NaiveMIPS SoC源代码 / brd-NSCSCC分支](https://git.net9.org/zhangyx13/NaiveMIPS-HDL/tree/brd-NSCSCC): ([NaiveMIPS SoC源代码在github上的备份](https://github.com/z4yx/NaiveMIPS-HDL))
* [NaiveMIPS软硬件设计文档](https://git.net9.org/zhangyx13/NaiveMIPS-HDL/raw/brd-NSCSCC/documentation/2017nscscc.pdf)：包含硬件实现及系统软件说明
* [Test cases for MIPS CPU implementation](https://github.com/oscourse-tsinghua/cpu-testcase/blob/master/README.md)
### 龙芯FPGA实验板上的ucore参考实现

* [ucore-thumips / for-NSCSCC分支](https://github.com/z4yx/ucore-thumips/tree/for-NSCSCC):与NaiveMIPS SoC搭配使用
* [ucore对于指令集及特权资源的说明](/doc/ucore_thumips.pdf)
* [硬件需求分析](/doc/ucore_requirements.pdf)

### 龙芯FPGA实验板上的Linux参考实现

* [Linux 4.6](https://git.net9.org/shanker/linux-naivemips) ：([Linux 4.6在github上的备份](https://github.com/z4yx/linux-kernel))配置方法参见`NaiveMIPS软硬件设计文档`
### 龙芯FPGA实验板上的U-Boot参考实现

* [U-Boot](https://github.com/z4yx/u-boot-naivemips) ：配置方法参见`NaiveMIPS软硬件设计文档`

### decaf交叉编译器参考实现

* [decaf-linux](https://git.net9.org/zhangyx13/decaf-linux)([decaf-linux在github上的备份](https://github.com/z4yx/decaf-linux))

### C0交叉编译器参考实现

* [C0编译器实现的代码和文档](http://os.cs.tsinghua.edu.cn/oscourse/csproject2014/group2#A.2BZwB.2ByE7jeAFTymKlVEo-)

### 与实验相关的其他问题和解决建议

* 实验箱PS/2接口线序错误，需要制作转接线修正


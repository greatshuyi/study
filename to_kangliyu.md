按照如下顺序学习参考 
 
 + [1] [7系列FPGA架构](http://www.eng.ucy.ac.cy/theocharides/Courses/ECE408/7%20Series%20FPGA%20Overview.pdf)
		只需要粗看，只需大致搞明白FPGA有哪些功能单元，物理上是如何组织的即可
		
 + [2] [V5 FPGA 架构概述](https://www.xilinx.com/support/documentation/data_sheets/ds100.pdf)
        只需要粗看，总结出和PCIE，高速Serdes的相关的功能Feature即可

 + [3] PCIE 2.0/3.0 Specification, PIPE Interface（自己下载一下）
         
        部分精读一下，总结关注几点
        1. PCIE层次结构，每层的功能特点，PCIE体系中的各种设备类型
        2. PIPE接口和功能
        3. 控制器与PIPE之间的互联与控制
		
 + [4] 搜索关于PCIE控制器设计的论文，找出其实现的架构并能够反向映射到[3]中SPEC给出的层次和接口最好，这里的重点实际上是要求明白控制器的设计架构
 
 + [5] [V5 高速IO的User Guide](https://www.xilinx.com/support/documentation/user_guides/ug196.pdf)
        
         部分精读一下，5、6、7三章：
         1. 搞懂TX/RX的结构，注意和[3] [4]所总结的层次结构和设计架构做一个映射，看此处V5 FPGA内部实现对应的是PCIE架构中的那一部分
         2. 总结一下TX/RX有哪些可配置功能点（后续功能设计实现依赖这个）

 + [6] [V5 PCIE Integrated Endpoint](https://www.xilinx.com/support/documentation/ip_documentation/pcie_blk_plus/v1_15/ug197.pdf)
         精读一下，总结一下
		 1. EDP Block的支持的功能和整体架构及其对应的PCIE架构中的位置
		 2. 在V5 FPGA中如何调用的（有大体概念即可，不用精通）

综上，经过这些阅读实际上要达到一个目的：
  
 + 1. 总结出FPGA内部高速接口，特别是PCIE接口控制器设计的功能规范
 + 2. 应该应用于FPGA内部的控制器架构做到大致清楚
 + 3. 应该提炼出可配置功能项
 + 4. 应大体有个应用现有IP构建和修改控制器的大致方向能够支撑大论文一到两章

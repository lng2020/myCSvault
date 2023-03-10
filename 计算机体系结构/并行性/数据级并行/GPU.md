## 思想
- ### 混合执行模式
	- CPU是主机，GPU是设备
- ### 集成开发环境CUDA(Compute Unified Device Architecture)
	- 将各种形式的GPU并行统一为CUDA线程(最低层次的并行性，并行性的基元)
- ### 编程模式
	- SIMT(Single Instruction Multiple Thread)
## NVIDA GPU
- ### 和[[向量机]]
	- #### 相似之处
		- 处理数据并行性问题都做得很好
		- 稀疏向量的集中分散转换
		- 向量掩模寄存器
		- 大容量寄存器堆
	- #### 不同之处
		- 没有标量处理器
		- GPU使用多线程隐藏存储器延迟(在处理一个线程的同时，从存储器读取另外一个线程的数据)
		- 拥有许多功能部件，不像向量机那样由少数深流水线部件构成
- ### 线程块调度器
	- 将线程块调度分配给不同的SIMD处理器
- ### SIMD处理器
- ### 寄存器
	- 通道分组，分配给各个通道使用
- ### 指令集架构
	- PTX(Parallel Thread Execution)指令就是CUDA线程涉及的操作
	- 指令格式
	- ![[Pasted image 20221223211717.png]]
- ### 存储器结构
	- #### 不在片上DRAM给每个SIMD通道提供了私有存储器
		- 每个通道的私有存储器不与其他通道共享
		- 私有存储器包含堆栈帧、私有变量等数据
		- 近期的GPU将上述数据缓存在L1和L2 Cache中
	- #### 每个多线程SIMD处理器同时包含片上局部存储器
		- 一个线程块的线程可以共享，SIMD通道也可以共享
	- #### GPU存储器
		- 不在片上，可以让不同SIMD处理器共享
		- CPU可以读写GPU存储器

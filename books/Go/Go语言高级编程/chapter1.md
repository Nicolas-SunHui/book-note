## 第1章 语言基础
- Go语言的并发编程哲学的口号：Do not communicate by sharing memory; instead, share memory by communicating.
- 数组
    - 数组是一个由固定长度的特定类型元素组成的序列，一个数组可以由0个或多个元素组成。
    - 数组的长度是数组类型的组成部分。
    - 数组定义

            var a [3]int //长度为3，[0, 0, 0]
            var b = [...]int{1,2,3} //长度为3
            var c = [...]int{2:3, 1:2} //长度为3 [0, 2, 3]
            var d = [...]int{1, 2, 4:5, 6} //长度为6[1, 2, 0, 0, 5, 6]
- 字符串
	- 一个字符串是一个不可改变的字节序列
	- 字符串的元素不可修改，是一个只读的字节数组
	- 字符串结构由两个信息组成：第一个是字符串指向的底层字节数组；第二个是字符串的字节的长度。
	- 字符串虽然不是切片，但是支持切片操作。
- Go语言的接口类型是延迟绑定，可以实现类似虚函数的多态功能。
- 当select()有多个分支时，会随机选择一个可用的通道分支，如果没有可用的通道分支，则选择default分支，否则会一直保持堵塞状态。

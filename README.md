# lab7

     本节目标：
          1. 循环的使用。
          2. 学习数组的使用。
          
获取及提交lab
-------
获取：通过 https://github.com/C-FUDAN-2020/lab7 获取。

提交物：将你完成目标1、目标2的源代码文件作为 lab7 的提交物。

提交：将提交物文档命名为学号_姓名 （如20302010000_王明），提交至超星学习通对应的作业中。

截止时间：北京时间 2020年11月08日 23:59:59

## 数组访问

> 请提交书面答案的文档

### 问题一
小明同学通过如下所示的代码来对若干数据进行求和。但是小明测试时发现如果输入的5个数据中最后一个数据是5时，计算结果不会出现错误；否则计算结果就是错误的。测试结果如图所示。请帮他分析产生这个现象的原因。

```c
#include <stdio.h>

int main(){
	int num[5];
	int sum = 0;
	for(int i = 1; i<= 5; i++){
		scanf("%d",&num[i]);
		printf("Number %d: %d\n",i,num[i]);
	}
	for(int i = 1; i <= 5; i++){
		sum += num[i];
	}
	printf("The sum is %d.",sum);
	return 0;
}
```
 <img src="./arrayAccess.png" width = "800" alt="测试实验" style="margin:0 auto" />

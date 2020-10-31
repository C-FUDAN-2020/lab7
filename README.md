# lab7

     本节目标：
          1. 练习循环语句与控制语句。
	  2. 学习数组的使用。
          3. PJ拆解。
          
获取及提交lab
-------
获取：通过 https://github.com/C-FUDAN-2020/lab7 获取。

提交物：将你完成目标1、目标2的源代码文件作为 lab7 的提交物。

提交：将提交物文档命名为学号_姓名 （如20302010000_王明），提交至超星学习通对应的作业中。

截止时间：北京时间 2020年11月08日 23:59:59

## 思考题目

> 请提交书面答案的文档

### 结构化编程
思考如下所示的代码会有怎样的控制台输出，并解释原因。

```c
#include <stdio.h>
int main(){
    int k=4;
    for(int i = 0; i < 3; i++){
        switch(k){
            default:
                k--;
                printf("It ");
            case 1:
                printf("is ");
                break;
            case 2:
                k++;
                printf("%d",2*k);
            case 3:
                k = k - i;
                printf("%d",3*(k<3?2:k));
                break;
            case 9:
                printf("%d",9*k);
                break;
        }
    }
    return 0;
}
```

### 数组访问
小明同学通过如下所示的代码来对若干数据进行求和。但是小明测试时输入5个数据`2 2 2 2 2`，得到的求和结果却是13，这显然不是正确的结果；接着小明又发现如果输入的5个数据中最后一个数据是5，得到的求和结果就不会出现错误。测试结果如图所示。请帮他分析产生这个现象的原因。

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
<div style="align: center">
    <img src="./arrayAccess.png" width="900" alt="测试结果"/>
</div>



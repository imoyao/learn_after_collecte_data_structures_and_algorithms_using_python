# 栈

## 概念
堆栈（stack）又称为`栈`或`堆叠`，是计算机科学中的一种抽象数据类型，只允许在有序的线性数据集合的一端（称为堆栈顶端，top）进行加入数据（push）和移除数据（pop）的运算。因而按照*后进先出* （LIFO, Last In First Out）的原理运作。
![后进先出](img/stack.png)
## 生活中的实例
- 弹夹（先压入的最后射出）
- 摞在一起的餐碟

![羽毛球杯](./img/stack-example.jpg)
（我们假设杯子只有顶端可以放入和取出）

## 操作
堆栈使用两种基本操作：推入（压栈，push）和弹出（弹栈，pop）：

推入：将数据放入堆栈顶端，堆栈顶端移到新放入的数据。
弹出：将堆栈顶端数据移除，堆栈顶端移到移除后的下一笔数据。
 
| 栈操作     | 当前栈中内容              | 返回值 | 说明             |
| ------------- | ------------------ | ------ | ------------------ |
| s.is_empty()  | []                 | True   | 判断是否为空 |
| s.push(4)     | [4]                |        | 推入             |
| s.push('dog') | [4,'dog']          |        |                    |
| s.peek()      | [4,'dog']          | 'dog'  | 返回栈顶项而不删除 |
| s.push(True)  | [4,'dog',True]     |        |                    |
| s.size()      | [4,'dog',True]     | 3      | 返回栈的项数 |
| s.is_empty()  | [4,'dog',True]     | False  |                    |
| s.push(8.4)   | [4,'dog',True,8.4] |        |                    |
| s.pop()       | [4,'dog',True]     | 8.4    | 从栈顶删除项 |
| s.pop()       | [4,'dog']          | True   |                    |
| s.size()      | [4,'dog']          | 2      |                    |

## 代码实现
[stack](stack.py)

## 其他
常与另一种有序的线性数据`队列`相提并论。
## 更多
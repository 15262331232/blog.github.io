---
title: Python Queue 和 Stack
tags: python Queue 编程 python3 Stack
categories: pymods
---



```
作者 jizy

此代码经 jizy 编写，未经许可，不得转载。
```

基本模板： 

无

安装：

Windows 版的Python只需到python.org下载安装包，安装即可。

```bash
#Python3的安装
$ yum install python3   #请在root下运行
#Linux 安装 pip
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py   # 下载安装脚本
$ sudo python get-pip.py    # 运行安装脚本
```

Queue代码：

```python
class Queue:
    def __init__(self):
        self.queue=[]

    def push(self,item):
        self.queue.append(item)

    def front(self):
        try:
            return self.queue[0]
        except IndexError:
            return None

    def pop(self):
        try:
            self.queue.pop(0)
        except IndexError:
            raise Exception("The queue is empty!")

```

Stack代码：

```python
class Stack:
    def __init__(self):
        self.stack=[]

    def push(self,item):
        self.stack.insert(0,item)

    def top(self):
        try:
            return self.stack[0]
        except IndexError:
            return None

    def pop(self):
        try:
            self.stack.pop(0)
        except IndexError:
            raise Exception("The stack is empty!")

```



原理：模拟了C++中的 Stack 和 Queue。
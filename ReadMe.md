# 代码规范
1. python文件，文件夹都是小写，单词之间用下滑线连接
2. 全局变量大写，局部变量小写，变量左右各空一个
3. 函数名小写，类首字母大写，驼峰
4. 注释，py文件注释顶行,三个双引号
5. 函数内各变量做注释，变量的类型，返回值

# 程序报错
1. 页面上的错误信息提示
2. pycharm中定位到错误行，排错 【建立错误信息博客积累】
3. 请求流程逐步分析

# 编写代码原则
1. 简单代码往上放，
2. 减少代码层级

[详情见:](https://www.cnblogs.com/sunxiuwen/p/9213125.html)

- 一、导包顺序
  1. 先标准库，内置
  2. 导入第三方
  3. 导入当前应用程序/库
  4. 不同分组之间以空行分割
  5. import 一次只导入一个模块
  6. 在一个模块中导入多个模块 from  xxx  import (a,b)
- 二、长度
  1. 一行最常79个字符

- 检查工具

  - 安装：pip3 install pep8   之后改名为pycodestyle，虽然还可以用，但执行时会提示用pycodestyle

    使用：pycodestyle  xx.py    会提示哪些不符合pep8标准

    加参数： --show-source   将会将不仅会显示错误且将原文件打出

- 格式化工具
  - 1. pycharm 自带，快捷键`ctrl+l`
    2. autopep8       pip3 install autopep8    atuopep8  xx.py
    3. black          pip3 install black       black xx.py
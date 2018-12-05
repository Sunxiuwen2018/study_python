# 单例模式

1. 通过__new__建立单利模式
```python

class SingleInstance(object):
    """单例模式"""
    _instance = None

    def __new__(cls, *args, **kwargs):
        if cls._instance is None:
            cls._instance = super().__new__(cls, *args, **kwargs)
        return cls._instance


class Me(object):
    """解决计算实例化了多少个实例"""
    _count = 0

    def __new__(cls, *args, **kwargs):
        cls._count += 1
        super().__new__(cls)
```

2. 导入模块也属于单例模式，因为解释器只会引入一次，重复导入没用
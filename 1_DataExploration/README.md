<h1 align = "center">:rocket: 数据探索性分析 :facepunch:</h1>

---
## 初始化设置
```python
import matplotlib.pyplot as plt
class Matplotlib(object):
    def __init__(self):
        """
        https://www.programcreek.com/python/example/4890/matplotlib.rcParams
        """
        pass

    def init_matplotlib(self):
        """初始化设置"""
        plt.style.use('ggplot')
        plt.rcParams['font.sans-serif'] = ['Microsoft YaHei'] # 中文乱码的处理
        plt.rcParams['axes.unicode_minus'] = False # 负号
        plt.rcParams["text.usetex"] = False
        plt.rcParams["legend.numpoints"] = 1
        plt.rcParams["figure.figsize"] = (10, 5)
        plt.rcParams["figure.dpi"] = 100
        plt.rcParams["savefig.dpi"] = plt.rcParams["figure.dpi"]
        plt.rcParams["font.size"] = 10
        plt.rcParams["pdf.fonttype"] = 42

    def clear_state(self):
        plt.close('all')
        plt.rcdefaults()
```
---
## [Seaborn][2]







---
[2]: https://github.com/Jie-Yuan/2_DataMining/tree/master/1_DataExploration/3_Seaborn

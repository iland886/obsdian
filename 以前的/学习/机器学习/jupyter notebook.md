### 逻辑回归
```python
from sklearn import datasets
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LogisticRegression
X = iris['data'][:,(2,3)]
log_res = LogisticRegression()
log_res.fit(X,y)

#棋盘表格
x0,x1=
np.meshgrid(np.linspace(2.8,7,500),np.linspace(0.2,5,200))
X_new = np.c_[x0.ravel(),x1.raval.()]
y_proba = log_res,predict_proba(X_new)
#画图操作
plt.plot(X[y == 0, 0],X[y == 0,1],'bs',label = 'Not Vitral')
plt.plot(X[y == 1, 0],X[y == 1,1],'r.',label = 'Vitral')  #选择是Vitral的第一个特征，第二个特征

#分类概率绘图
zz = y_proba[:,1].reshape(x0.shape)   #是Vitral花的概率
plt.contour(x0, x1, zz,cmap = plt.cm.brg)
plt.show()

```
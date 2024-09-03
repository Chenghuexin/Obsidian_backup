---
media: https://www.youtube.com/watch?v=QW6uINn7uGk
---
# 原本我們以為Optimization會失敗的原因 : 

當參數對loss的微分為0時，gradient descent無法再更新參數，卡在local minima

# 事實上...

導致gradient是0的原因不只有local minima，還有saddle point

- saddle point : gradient is zero, but it's neither local minima nor local maxima
- critical point : all point when their gradient are zero

# 如何判斷是走到local minima還是sa
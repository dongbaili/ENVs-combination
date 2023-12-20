## common setting
- distance metric: MMD
- n_train: 800
## 优化
- 每个环境一个weight，加权中心点
- 线性模型 + l1 正则化
- 排序后的weight大致效果如下
<div style="display: flex;">
<img src="weights/NY_1.png" alt="" width="400">
<img src="weights/WA_2.png" alt="" width="400">
</div>
选weight最大的三个环境作为训练组合
(重复三次实验取表现最好的)

- 图示的是我们的方法和其他方法之间的差值

ACSIncome_OH
<div style="display: flex;">
<img src="mmd/ACSIncome_OH.png" alt="" width="400">
</div>

ACSIncome_TX
<div style="display: flex;">
<img src="mmd/ACSIncome_TX.png" alt="" width="400">
</div>

ACSPublicCoverage_WA
<div style="display: flex;">
<img src="mmd/ACSPublicCoverage_WA.png" alt="" width="400">
</div>

## 问题
- 每次优化出来的结果不是很稳定
- 需要选择几次重复实验中的好者才能明显比各个baseline都好，需要更多调参
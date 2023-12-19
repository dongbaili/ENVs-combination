## common setting
- distance metric: MMD
- n_train: 800
- 图示的是我们的方法和其他方法之间的差值
## 遍历
50选3，遍历算组合距离，取最近的进行测试

ACSIncome_OH
<div style="display: flex;">
<img src="direct/ACSIncome_OH.png" alt="" width="400">
</div>

ACSIncome_TX
<div style="display: flex;">
<img src="direct/ACSIncome_TX.png" alt="" width="400">
</div>

ACSPublicCoverage_WA
<div style="display: flex;">
<img src="direct/ACSPublicCoverage_WA.png" alt="" width="400">
</div>

## 优化
- 每个环境一个weight，加权中心点
- 线性模型 + l1 正则化
- 排序后的weight大致效果如下
<div style="display: flex;">
<img src="weights/NY_1.png" alt="" width="400">
<img src="weights/WA_2.png" alt="" width="400">
</div>
选weight最大的三个环境测试
(重复三次取最好)

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
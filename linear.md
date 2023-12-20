# Settings

3 * 800 vs 49 * 50
由于表现不稳定，进行20次重复实验取平均

Linear model

- top3是单独计算距离，排序后将前三个组合
- best是C10 3遍历出来的最优组合
- 50是49个环境每个50个样本
---
ACSIncome_OH
<div style="display: flex;">
<img src="linear/ACSIncome_OH_uda_accuracy_50.png" alt="" width="400">
<img src="linear/ACSIncome_OH_uda_f1_50.png" alt="" width="400">
</div>
ACSIncome_TX
<div style="display: flex;">
<img src="linear/ACSIncome_TX_uda_accuracy_50.png" alt="" width="400">
<img src="linear/ACSIncome_TX_uda_f1_50.png" alt="" width="400">
</div>
ACSEmployment_NY
<div style="display: flex;">
<img src="linear/ACSEmployment_NY_uda_accuracy_50.png" alt="" width="400">
<img src="linear/ACSEmployment_NY_uda_f1_50.png" alt="" width="400">
</div>
ACSPublicCoverage_WA
<div style="display: flex;">
<img src="linear/ACSPublicCoverage_WA_uda_accuracy_50.png" alt="" width="400">
<img src="linear/ACSPublicCoverage_WA_uda_f1_50.png" alt="" width="400">
</div>

## 初步结论： best > 49 * 50 > 012
- 通过某种距离metric，C10 3 遍历出最近的组合
（结果不稳定，取组合距离最小的三组的最优表现）
- 左边三个是mmd距离选出的组合表现，中间三个是wasserstein距离，右边三个是cosine similarity
- 计算目标组合和对应的baseline之间的差值
  
ACSIncome_OH
<div style="display: flex;">
<img src="gap/Gap_ACSIncome_OH.png" alt="" width="400">
</div>
ACSIncome_TX
<div style="display: flex;">
<img src="gap/Gap_ACSIncome_TX.png" alt="" width="400">
</div>
ACSEmployment_NY
<div style="display: flex;">
<img src="gap/Gap_ACSEmployment_NY.png" alt="" width="400">
</div>
ACSPublicCoverage_WA
<div style="display: flex;">
<img src="gap/Gap_ACSPublicCoverage_WA.png" alt="" width="400">
</div>


# 🚀 Tmall Repeat Purchase Prediction

## 🧠 Project One-liner
基于天猫用户行为日志数据（数据过大未上传，可官方下载），构建 XGBoost 复购预测模型，通过行为特征工程与转化率建模，实现用户未来6个月复购概率预测（AUC=0.6532），用于精准营销与用户分层。

---

## ⭐ Project Highlights

- 构建300万级用户行为日志特征工程体系
- 设计点击 / 加购 / 收藏 / 购买转化率特征
- 完成用户 × 商家粒度建模（User-Merchant Level）
- 使用XGBoost完成二分类建模与调优
- 模型AUC从0.64 → 0.6532
- 输出用户复购概率用于业务决策

---

## 📌 STAR 项目表达

### 🟦 S（Situation）
电商平台存在大量用户“一次性购买后流失”问题，导致营销ROI低下。

### 🟦 T（Task）
构建用户复购预测模型，识别高潜力复购用户，实现精准营销。

### 🟦 A（Action）
- 清洗并整合300万+用户行为日志
- 构建用户-商家交互特征（click/cart/buy/fav）
- 设计转化率特征（click2buy、cart2buy等）
- 构建用户画像（年龄、性别）
- 使用XGBoost训练模型并调参优化

### 🟦 R（Result）
- AUC提升至0.6532
- 成功识别高价值复购用户
- 支持用户分层与精准营销

---

## 📈 Model Performance Evolution

| Version | Feature Strategy | AUC |
|--------|------------------|------|
| Baseline | 原始行为计数 | 0.6407 |
| V1 | +转化率特征 | 0.6412 |
| Final | +行为结构 +正则化优化 | 0.6532 |

---

## 📊 Feature Importance Interpretation

### 🥇 商家因素
- merchant_buy_rate
- m_buy_cnt
- m_user_cnt

### 🥈 用户行为强度
- buy_cnt
- click
- cart

### 🥉 转化率特征
- cart2buy
- click2buy

---

## 📊 Key Business Insights

- 用户流失集中在点击阶段
- 商家质量影响复购
- 行为结构比行为数量更重要
- 用户活跃度 = 长期价值核心指标

---

## 📉 Model Evaluation

| Metric | Score |
|--------|------|
| AUC | 0.6532 |

---

## 📊 Visualizations

- Feature Importance
- ROC Curve
- Gender Distribution
- Repurchase Rate by Age
- Repurchase Rate by Gender

---

## 📊 Visualizations（已在项目中实现）

### 1. 特征重要性

images/feature_importance.png

### 2. ROC 曲线

images/roc_curve.png

### 3. 用户画像与复购分析

images/gender_distribution.png

images/repurchase_rate_by_age.png

images/repurchase_rate_by_gender.png

---

## ❓ Interview Questions

**Q1：为什么用AUC？**  
A：类别不平衡问题严重

**Q2：最重要特征？**  
A：转化率特征（cart2buy）

**Q3：为什么XGBoost？**  
A：非线性 + 稳定 + 工业级常用

---

## 🧱 Project Structure

```

Tmall-Repeat-Purchase/
├── data/
├── images/
├── report/
├── output/
├── main.ipynb
├── README.md

```
---

## 🚀 Final Conclusion

本项目完整实现电商复购预测流程：

数据处理 → 特征工程 → 模型训练 → 调参优化 → 可视化分析

最终AUC=0.6532，具备实际业务应用价值。

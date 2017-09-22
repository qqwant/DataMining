# :rocket: Xgboost参数解释 :facepunch:
---
- objective

|objective|定义学习任务及相应的学习目标|
|:--|:--|
|reg:linear|线性回归
|reg:logistic|逻辑回归
|binary:logistic|二分类的逻辑回归问题，输出为概率
|binary:logitraw|二分类的逻辑回归问题，输出的结果为wTx
|count:poisson|计数问题的poisson回归，输出结果为poisson分布 在poisson回归中，max_delta_step的缺省值为0.7(used to safeguard optimization)
|multi:softmax|让XGBoost采用softmax目标函数处理多分类问题，同时需要设置参数num_class（类别个数）
|multi:softprob|和softmax一样，但是输出的是ndata * nclass的向量，可以将该向量reshape成ndata行nclass列的矩阵没行数据表示样本所属于每个类别的概率
|rank:pairwise|set XGBoost to do ranking task by minimizing the pairwise loss
---
- eval_metric

|eval_metric|评估指标|
|:--|:--|
|rmse| root mean square error
|logloss| negative log-likelihood
|error| Binary classification error rate. It is calculated as #(wrong cases)/#(all cases). For the predictions, the evaluation will regard the instances with prediction value larger than 0.5 as positive instances, and the others as negative instances.
|merror| Multiclass classification error rate. It is calculated as #(wrong cases)/#(all cases).
|mlogloss| Multiclass logloss
|auc| Area under the curve for ranking evaluation.
|ndcg|Normalized Discounted Cumulative Gain
|map|Mean average precision
|ndcg@n/map@n| n can be assigned as an integer to cut off the top positions in the lists for evaluation.
|ndcg-map-/ndcg@n-/map@n-/|In XGBoost, NDCG and MAP will evaluate the score of a list without any positive samples as 1. By adding “-” in the evaluation metric XGBoost will evaluate these score as 0 to be consistent under some conditions.
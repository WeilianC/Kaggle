运行步骤
1 下载数据集 （https://www.kaggle.com/competitions/open-problems-multimodal/data）到data文件夹 open-problems-multimodal 路径下
   下载数据集（https://www.kaggle.com/datasets/fabiencrom/multimodal-single-cell-as-sparse-matrix）到data文件夹 multimodal-single-cell-as-sparse-matrix路径下
   下载数据集（https://www.kaggle.com/datasets/senkin13/single-cell-features）到data文件夹 single_cell_features路径下
2 运行code/fe_process_cite.py和code/fe_process_multi.py文件，该步骤主要目的是生成cite任务和multi任务的特征文件，运行需要一定时间
3 运行code/cite-lgb.py，这个代码训练lgb预测 cite 任务
4 运行code/gru-cite.py，这个代码训练gru预测 cite 任务
5 运行code/multi-mlp.py，这个代码训练mlp预测multi任务
6 运行code/infer.ipynb，得到拼接结果
7 提交result/sub/submission.csv文件到kaggle


一些依赖的包需要自行安装一下
pandas
numpy
lightgbm
pyarrow
torch
pickle
tdqm
tables

运行需要内存较大，建议64G内存+GPU显卡






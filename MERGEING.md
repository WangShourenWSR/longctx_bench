# 要点：
运行一遍longbench，首先主要追踪在eval_longbench.py中，config这一参数的行为：
1. 它是如何被加载的
2. 它是如何被分配给各个pipeline函数的
3. 做好笔记和注释，以便于将helmet的代码分配过来。

# 发现
每一个脚本只运行一个数据集和一个模型。和HELMET不一样，HELMET直接运行同一task下的所有数据集


# Adding files
1. pipeline_config/baseline/ms_icl/******.json
2. eval_config/baseline
3. pipeline/baseline/eval_ms_icl.py


# Config files
## config/eval_config/longbench
这个文件指定了数据集、instructions、metrics等，以及output的设置
## config/pipeline_config/baseline/longbench
这个文件指定了模型的设置

## config/

# Datasets
## Merging
The datasets of HELMET being merged should be like Few-shot learning tasks in LongBench, which including TriviaQA, SAMSum, and TREC.

## config files
详见: dataset/longbench/...
似乎只提及了下载，没有提及别的。
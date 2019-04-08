## 文件组织

- code
	- **anomaly injection.ipynb** : 异常注入源码（逻辑错误的版本一，时间戳和根因分别随机选取，使得出现随机的时间戳中没有对应根因的情况）；
	- **version2** ： 改正之后的异常注入源码。

- data
	- **anomaly** ： 异常注入源码运行后————在随机timestamp上，为随机生成的25种根因注入异常，将总异常值平均分发到此其在timestamp上的所有后代叶子元素中；
	- **origin** ： 原始KPI数据集第2周数据，按时间戳划分；
	- **result** ： 按第layer 1 ；属性值划分数据集，每个属性每个值对应的KPI时间序列（用于版本一）；
	- **timestamp_root_cause**： 注入异常的每个时间戳对应的根因集（版本一结果）；
	- **abnormal_timestamps.csv**：注入异常的25个时间戳（版本一结果）；
	- **KPI_new.csv** ： 每个时间戳的总KPI;
	- **KPI_week2.csv** ： 每个时间戳的总KPI（第二周）;
	- **root_causes.npy** ： 异常注入源码运行后————随机生成的25种根因数组保存成文件，便于定位根因的结果评估（版本一结果）；
	- **timestamps_root_causes.csv**： 异常注入的timestamp与根因一一对应的dataframe（版本二结果）。
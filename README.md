# DB-meets-AI
AI and DB can benefit from each other. Hence, the project contains documentation about the two.

本项目包含AI与DB结合领域的资料，主要包括AI4DB、DB4AI以及AI in DB三大领域。

## AI4DB
使用AI的手段来达成数据库等基础软件的自治运维能力，如索引推荐、参数调优以及故障诊断等。

## DB4AI
通过数据库实现AI模型的训练和管理，也即 in-database machine learning.

### 益处

1. "Be close to your data.": Keeping the code near the data is necessary to keep the latency low; 有助于减少数据传输延迟。
2. 更安全：数据统一管理，利用数据库自身严格的安全以及审计机制，确保数据泄露可能的最小化；
3. 更快速：将模型优化能力整合在数据库内，充分挖掘向量化执行、GPU、NUMA等机制的性能提升；
4. 更易用：提供开箱即用的AI能力，用户可以不关注算法的实现，只需关注模型的训练和使用，聚焦于业务成功；
5. 易管理：防止模型存储碎片化，提供集中式的模型、数据管理能力，防止模型存储的碎片化；
6. 天然的AP特性：原始OLAP能力只能提供数据的统计和分析，通过AI功能，补足OLAP系统的在预测能力上的不足。

### 典型的具备库内AI能力的数据库

1. Amazon Redshift: Amazon Redshift ML is designed to make it easy for SQL users to create, train, and deploy machine learning models using SQL commands. 
2. BlazingSQL: BlazingSQL is a GPU-accelerated SQL engine built on top of the RAPIDS ecosystem; it exists as an open-source project and a paid service.
3. Google Cloud BigQuery: BigQuery ML brings much of the power of Google Cloud Machine Learning into the BigQuery data warehouse with SQL syntax, without extracting the data from the data warehouse.
4. IBM Db2 Warehouse: IBM Db2 Warehouse includes a wide set of in-database SQL analytics that includes some basic machine learning functionality, plus in-database support for R and Python.
5. Kinetica: Kinetica provides a full in-database lifecycle solution for machine learning accelerated by GPUs, and can calculate features from streaming data.
6. Microsoft SQL Server: Current versions of SQL Server can train and infer machine learning models in multiple programming languages.
7. Oracle Database: Oracle Cloud Infrastructure can host data science resources integrated with its data warehouse, object store, and functions, allowing for a full model development lifecycle (AutoML, ML, DL).
8. Vertica: Vertica has a nice set of machine learning algorithms built-in, and can import TensorFlow and PMML models.
9. MindsDB: MindsDB brings useful machine learning capabilities to a number of databases that lack built-in support for machine learning.
10. MADlib: An extension to PostgreSQL. It contains a lot of AI algorithms, not only machine learning but also deep learning and algorithm utility. PostgreSQL-based databases (e.g., Greenplum, PGXL) can be easy to integrate to get AI abilities.
11. openGauss: An open-sourced database in China, which Huawei released. In the openGauss, there are some machine learning algorithms built-in. Also, it features several training utilities, such as DB4AI-snapshots. 
12. SQLflow: It is a SQL syntax model training tool that does not support data storage, merely simplifying programming. 

# 典型技术
1. 向量化执行
2. 并行执行
3. 新硬件（如GPU）加速
4. 高效率的AI算法集成形态（不是简单的UDF形式）
5. 模型管理
6. 全流程的AI工具：如超参数优化
7. 提供开箱即用的SQL语法
8. 分布式训练：如参数服务器、联邦学习等技术的吸收
9. 高效的数据存储：如列存
10. 模型的导入与导出：支持对常用框架格式的支持，如tensorflow、Pytorch


### 参考资料

- https://www.infoworld.com/article/3607762/8-databases-supporting-in-database-machine-learning.html
- https://madlib.apache.org/
- https://opengauss.org/zh/

## AI in DB
通过改造现有的数据库结构，融合AI相关的算法，实现数据库性能、易用性、安全性等的提升。


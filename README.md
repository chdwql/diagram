```plantuml
@startuml
title 周月会商邻省异常APNET抓取、分布图绘制自动化

start

:数据抓取;
:使用Python的requests库从APNET网站抓取邻省异常数据;
:解析数据格式（如JSON、XML），提取所需信息;

:数据存储;
:将抓取的数据存储在本地数据库（如MySQL或PostgreSQL）;

:数据处理;
:编写数据处理脚本，清洗并整理数据，确保格式统一、无误;

:图形绘制;
:使用GMT或PyGMT生成各学科异常的空间分布图;

:自动化流程;
:将上述过程整合为自动化工作流，利用定时任务（如cron job）定期运行;

stop
@enduml

```plantuml
@startuml
title 震后应急会商地球物理各学科震后应急产品自动化产出

start

:抓取地震目录;
:从省局EQIM实时抓取最新地震信息，达到对应震级后触发;

:获取前兆异常分布;
:根据震中位置，利用addereq抓取周边台站、异常测项分布数据;
:使用GMT绘制分布图;

:产品生成;
:利用addereq抓取周边100km（半径根据震级自动调整）前兆数据;
:自动生成震后应急所需的各类图表和报告;

stop
@enduml

```plantuml
@startuml
title 新增干扰源对现有站网的影响自动化评估

start

:干扰源数据获取;
:从设计单位获取奥维数据，自动产出干扰源的位置信息;

:影响评估模型;
:根据国家环境保护标准，构建评估模型，量化干扰源对地震监测站网的影响;

:自动化评估;
:编写Python脚本，结合GIS工具（如QGIS、ArcGIS），实现干扰源影响的自动化评估;

stop
@enduml

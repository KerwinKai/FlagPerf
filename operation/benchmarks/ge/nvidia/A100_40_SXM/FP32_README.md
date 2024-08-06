# 参评AI芯片信息

* 厂商：Nvidia

* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1
* 单服务器内使用卡数: 1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID: 801377f03ba4649bc2d839ff34e38be66ee8a633

# 评测结果

## 核心评测结果

| 评测项  | correctness | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | : True    | 0.16TFLOPS       | 0.16TFLOPS        | 0.81% | 0.8% |
| nativetorch | : True    | 0.16TFLOPS      | 0.16TFLOPS      | 0.81%      | 0.81%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 6822.21us       | 6840.32us        | 146.58op/s | 146.19op/s | 1484940.19us | 6922.37us |
| nativetorch | 6778.9us       | 6796.29us        | 147.52op/s | 147.14op/s | 21901.5us | 6805.13us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1599.0W | 1638.0W | 67.55W   | /     | 263.16W       | 268.0W      | 3.17W        | 400W  |
| flaggems监控结果 | 1657.5W | 1716.0W | 101.32W   | /     | 287.93W       | 290.0W      | 2.69W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.75%    | 2.495%   | 48.17°C       | 27.499%        |
| flaggems监控结果 | 0.699%    | 2.491%   | 49.41°C       | 30.025%        |
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
| flaggems | True    | 255.52TFLOPS       | 258.3TFLOPS        | 81.9% | 82.79% |
| nativetorch | True    | 255.94TFLOPS      | 257.62TFLOPS      | 82.03%      | 82.57%    |

## 其他评测结果

| 评测项  | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | 
| flaggems | 4302.98us       | 4256.77us        | 232.4op/s | 234.92op/s | 21432134.56us | 4219.83us |
| nativetorch | 4296.02us       | 4268.03us        | 232.77op/s | 234.3op/s | 184282.1us | 4428.74us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1495.0W | 1872.0W | 138.19W   | /     | 396.67W       | 407.0W      | 4.2W        | 400W  |
| flaggems监控结果 | 1495.0W | 1872.0W | 130.65W   | /     | 399.71W       | 417.0W      | 6.78W        | 400W  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.84%    | 2.648%   | 64.56°C       | 7.181%        |
| flaggems监控结果 | 0.912%    | 2.857%   | 64.11°C       | 7.181%        |

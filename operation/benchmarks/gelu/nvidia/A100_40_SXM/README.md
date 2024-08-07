# 参评AI芯片信息

* 厂商：Nvidia


* 产品名称：A100
* 产品型号：A100-40GiB-SXM
* TDP：400W

# 所用服务器配置

* 服务器数量：1


* 单服务器内使用卡数：1
* 服务器型号：DGX A100
* 操作系统版本：Ubuntu 20.04.4 LTS
* 操作系统内核：linux5.4.0-113
* CPU：AMD EPYC7742-64core
* docker版本：20.10.16
* 内存：1TiB
* 服务器间AI芯片直连规格及带宽：此评测项不涉及服务期间AI芯片直连

# 算子库版本

https://github.com/FlagOpen/FlagGems. Commit ID:9168f2d031ecc1b31a9f658fb66dd6735b7306b3

# 评测结果

## 核心评测结果

| 评测项  | 平均相对误差(with FP64-CPU) | TFLOPS(cpu wall clock) | TFLOPS(kernel clock) | FU(FLOPS Utilization)-cputime | FU-kerneltime |
| ---- | -------------- | -------------- | ------------ | ------ | ----- |
| flaggems | 1.80E-07    | 1.57TFLOPS       | 1.57TFLOPS        | 8.07% | 8.06% |
| nativetorch | 2.15E-07    | 1.57TFLOPS      | 1.57TFLOPS      | 8.07%      | 8.07%    |

## 其他评测结果

| 评测项  | 相对误差(with FP64-CPU)标准差 | cputime | kerneltime | cputime吞吐 | kerneltime吞吐 | 无预热时延 | 预热后时延 |
| ---- | -------------- | -------------- | ------------ | ------------ | -------------- | -------------- | ------------ |
| flaggems | 3.87E-07    | 6139.86us       | 6145.02us        | 162.87op/s | 162.73op/s | 314473.94us | 6205.19us |
| nativetorch | 4.20E-07    | 6138.4us       | 6141.95us        | 162.91op/s | 162.81op/s | 10541.9us | 6156.06us |

## 能耗监控结果

| 监控项  | 系统平均功耗  | 系统最大功耗  | 系统功耗标准差 | 单机TDP | 单卡平均功耗 | 单卡最大功耗 | 单卡功耗标准差 | 单卡TDP |
| ---- | ------- | ------- | ------- | ----- | ------------ | ------------ | ------------- | ----- |
| nativetorch监控结果 | 1716.0W | 1716.0W | 0.0W   | /     | 325.77W       | 329.0W      | 5.39W        | 1716.0  |
| flaggems监控结果 | 1794.0W | 1794.0W | 0.0W   | /     | 373.03W       | 379.0W      | 4.64W        | 1794.0  |

## 其他重要监控结果

| 监控项  | 系统平均CPU占用 | 系统平均内存占用 | 单卡平均温度 | 单卡最大显存占用 |
| ---- | --------- | -------- | ------------ | -------------- |
| nativetorch监控结果 | 0.798%    | 1.396%   | 52.73°C       | 41.64%        |
| flaggems监控结果 | 0.768%    | 1.396%   | 54.92°C       | 31.352%        |

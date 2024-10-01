
# pip时由于目标计算机积极拒绝，无法连接网络问题解决

## 操作系统
Windows 10

## Python版本
3.12

## 问题描述

在终端中输入：
```bash
pip install {模块名}
```
得到反馈（以pygame为例）：
```sql
WARNING: Retrying (Retry(total=0, connect=None, read=None, redirect=None, status=None)) after connection broken by 'ProxyError('Cannot connect to proxy.',
 NewConnectionError('<pip._vendor.urllib3.connection.HTTPSConnection object at 0x0000021FC8D246E0>: Failed to establish a new connection: [WinError 10061] 由于目标计算机积极拒绝，无法连接网络。'))': /simple/pygame/
ERROR: Could not find a version that satisfies the requirement pygame (from versions: none)
ERROR: No matching distribution found for pygame
```
### 初步解决方案

-   关闭代理配置
-   更新 pip
-   使用镜像网站

**结果：**反馈依旧如上
### 最终解决方案

（以下回答来自 ChatGPT）

检查网络代理设置：虽然你已经尝试关闭代理，但有时系统或 pip 配置中可能仍有残留的代理设置。可以尝试以下命令来检查和清除 pip 的代理配置：
```bash
pip config unset global.proxy
```
**结果：**再次尝试后执行成功


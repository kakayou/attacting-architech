# windows10安装tensorflow 的cpu版本
## 依赖环境
windows10
python 3.7

## 安装c++ 库

[vc_redist.x64.exe](https://support.microsoft.com/zh-cn/help/2977003/the-latest-supported-visual-c-downloads)

## 配置pip镜像
创建C:\Users\{{用户名}}\pip\pip.ini 文件，并添加如下配置
<code>
[global]
index-url = http://mirrors.aliyun.com/pypi/simple/
[install]
trusted-host=mirrors.aliyun.com
</code>

## 安装
<code>pip install tensorflow-cpu</code>

## 测试
<code>
import tensorflow as tf
print(f"tensorflow version = {tf.__version__}", end='\n\n')
</code>
输出结果如下：
tensorflow version = 2.2.0
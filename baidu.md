1.tensorflow安装

按照tensorflow中文社区的提示，我使用二进制安装，通过python中的pip安装。

因为我下的是最新python3.7版本，所以我在终端的操作与pip相关的后面都加了个3，安装了很久提示

Could not find a version that satisfies the requirement tensorflow (from versions: )

No matching distribution found for tensorflow

You are using pip version 10.0.1, however version 18.1 is available.

You should consider upgrading via the 'pip install --upgrade pip' command.

再仔细检查根据老师提示输入python3检查发现3.7版本不支持安装tensorflow。

然后改装2.7版本，将pip升级到最新安装，下载到最后提示

matplotlib 1.3.1 requires nose, which is not installed.

matplotlib 1.3.1 requires tornado, which is not installed.

按照终端提示打开了pip 与bin的读写权限。重新安装出现以下情况。



Cannot uninstall 'numpy'. It is a distutils installed project and thus we cannot accurately determine which files belong to it which would lead to only a partial uninstall.

根据网上提示

(sudo pip install numpy --ignore-installed numpy)

测试tensorflow import tensorflow 显示找不到…


最后根据学长提示安装了brew 下载了python3.6.5

安装成功YizhedeMacBook-Pro:~ yizhechen$ python3

Python 3.6.5 (default, Jun 17 2018, 12:13:06) 

[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.2)] on darwin

Type "help", "copyright", "credits" or "license" for more information.

>>> import tensorflow as tf

>>> hello = tf.constant('Hello, TensorFlow!')

>>> sess = tf.Session()

2018-10-31 20:31:55.452258: I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA

>>> print(sess.run(hello))

b'Hello, TensorFlow!'

YizhedeMacBook-Pro:~ yizhechen$ python3

Python 3.6.5 (default, Jun 17 2018, 12:13:06) 

[GCC 4.2.1 Compatible Apple LLVM 9.1.0 (clang-902.0.39.2)] on darwin

Type "help", "copyright", "credits" or "license" for more information.

>>> import tensorflow as tf

>>> hello = tf.constant('Hello, TensorFlow!')

>>> sess = tf.Session()

2018-10-31 20:31:55.452258: I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA

>>> print(sess.run(hello))

b'Hello, TensorFlow!'



2.MNIST
首先在tensorflow中文社区上下载MINST训练集数据，需要登陆google一开始不知为什么，gmail号被封了，申请恢复。
后来账号还是没有恢复，我通过其他渠道下载了数据。
按照网上指导代码在python中使用tensorflow实现了对数据集的分类。



2021.6.2 github desktop
参考源码：  **[LapDepth-release](https://github.com/tjqansthd/LapDepth-release)**

数据集下载链接在datasets的kitti_archives_to_download.txt中，建议用Notepad++打开，这样双击链接就下载了。 下载好放在datatsets/KITTI里解压就行

eigen_test_files_with_gt_dense-bac.txt和eigen_train_files_with_gt_dense-bac.txt分别是完整的测试集和训练集目录。我自己从里面抽了2011_09_26_drive_0001_sync和2011_09_26_drive_0005_sync作为训练集，2011_09_26_drive_0002_sync作为测试集，写在了eigen_train_files_with_gt_dense.txt和eigen_test_files_with_gt_dense.txt里。如果你觉得数据不够就将这两文件内容改一下就好了，或者你直接用完整版的，把后面的-bac删掉就好。

需要自己下载深度估计标注数据：http://www.cvlibs.net/download.php?file=data_depth_annotated.zip

这个外网贼难下，我提供了夸克链接（里面包含了LDRN_KITTI_ResNext101_pretrained_data.pkl）：https://pan.quark.cn/s/8b10d41a3824

下载好放在datatsets/KITTI里解压就行

**在windows系统里运行一定会报错！！！**

首先你需要pip install windows-curses

需要新建一个fcntl.py放在你的lib目录下，这个文件我放在安装里了。如果你跟我一样建了虚拟环境的话，不然直接放在anaconda3/Lib就行。

<img width="471" alt="9d8cf55747261b7f2b2293765ff001c" src="https://github.com/user-attachments/assets/7a169015-6292-46c2-b2e3-5f895aaf2d0c">


其它报错你运行一下，报错就pip install一下，然后在blessings里会有个报错，在blessings中注释掉 #from termios import TIOCGWINSZ，因为这个是linux里的东西，windows用不了。

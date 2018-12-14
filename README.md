# dl_tips
1. some deep learning installation tips

1) installation env: 
a) win10+anaconda3 4.2.0(py3.5.2)+cuda8.0+cudnn6.0+tensorflow_gpu1.4.0
b) win10+anaconda3 4.2.0(py3.5.2)+cuda9.0+cudnn7.0+tensorflow_gpu1.7.0

2) how to install tensorflow in python if it is installed in C:/ and whihout enough authority?
use powershell and right-click to open it in adminstrator authority

3) how to solve the problem that .py with chinese characters cannot be run in shell?
add [#encoding=utf-8] at the head of .py and make sure it is in utf-8 encoding

4) make sure your GPU drivers have been updated, or it may lead to some ridiculous problems

5) fail in loading tensorflow model from others and recall "Cannot assign a device for operation..."
fix: https://blog.csdn.net/luxgang/article/details/83116564
use [sess = tf.Session(config=tf.ConfigProto(allow_soft_placement=True, log_device_placement=True))] to replace [sess = tf.Session()]

# learn_notes
## W3C SCHOOL 词典  
https://www.w3cschool.cn/dict/  
# numpy
e=np.eye(3);e
array([[ 1.,  0.,  0.],
       [ 0.,  1.,  0.],
       [ 0.,  0.,  1.]])
       
np.pad（）常用与深度学习中的数据预处理，可以将numpy数组按指定的方法填充成指定的形状

tf.matmul():矩阵乘法

* np.multiply() 元素乘法

* np.squeeze() 可以直接进行压缩维度


# matplotlib
* 图片显示
 index = 11
plt.imshow(X_train_orig[index])
print("Y = " + str(np.squeeze(Y_train_orig[:,index])))

# keras
* 打开图片
from keras.preprocessing import image  
from matplotlib.pyplot import imshow  
img_path = 'images/my_image.jpg'  
img = image.load_img(img_path, target_size=(64, 64))  
imshow(img)  
* K.learning_phase()  
返回训练模式/测试模式的flag，该flag是一个用以传入Keras模型的标记，以决定当前模型执行于训练模式下还是测试模式下.  

# tensorflow
keras与tensorflow联合编程  
tf.cast(x, dtype, name=None)  将x的数据格式转化成dtype  
* Tensorflow一些常用基本概念与函数  
https://blog.csdn.net/lenbow/article/details/52152766  
* 速查词典  
https://www.w3cschool.cn/doc_tensorflow_python/dict  

# os.path  
os.path包含了很多文件、文件夹操作的方法。下面列出：

os.path.abspath(path) #返回绝对路径  
os.path.basename(path) #返回文件名  
os.path.commonprefix(list) #返回多个路径中，所有path共有的最长的路径。  
os.path.dirname(path) #返回文件路径  
os.path.exists(path)  #路径存在则返回True,路径损坏返回False  
os.path.lexists  #路径存在则返回True,路径损坏也返回True  
os.path.expanduser(path)  #把path中包含的"~"和"~user"转换成用户目录  
os.path.expandvars(path)  #根据环境变量的值替换path中包含的”$name”和”${name}”  
os.path.getatime(path)  #返回最后一次进入此path的时间。  
os.path.getmtime(path)  #返回在此path下最后一次修改的时间。  
os.path.getctime(path)  #返回path的大小  
os.path.getsize(path)  #返回文件大小，如果文件不存在就返回错误  
os.path.isabs(path)  #判断是否为绝对路径  
os.path.isfile(path)  #判断路径是否为文件  
os.path.isdir(path)  #判断路径是否为目录  
os.path.islink(path)  #判断路径是否为链接  
os.path.ismount(path)  #判断路径是否为挂载点（）  
os.path.join(path1[, path2[, ...]])  #把目录和文件名合成一个路径  
os.path.normcase(path)  #转换path的大小写和斜杠  
os.path.normpath(path)  #规范path字符串形式  
os.path.realpath(path)  #返回path的真实路径  
os.path.relpath(path[, start])  #从start开始计算相对路径  
os.path.samefile(path1, path2)  #判断目录或文件是否相同  
os.path.sameopenfile(fp1, fp2)  #判断fp1和fp2是否指向同一文件  
os.path.samestat(stat1, stat2)  #判断stat tuple stat1和stat2是否指向同一个文件  
os.path.split(path)  #把路径分割成dirname和basename，返回一个元组  
os.path.splitdrive(path)   #一般用在windows下，返回驱动器名和路径组成的元组  
os.path.splitext(path)  #分割路径，返回路径名和文件扩展名的元组  
os.path.splitunc(path)  #把路径分割为加载点与文件  
os.path.walk(path, visit, arg)  #遍历path，进入每个目录都调用visit函数，visit函数必须有3个参数(arg, dirname, names)，dirname表示当前目录的目录名，names代表当前目录下的所有文件名，args则为walk的第三个参数  
os.path.supports_unicode_filenames  #设置是否支持unicode路径名  

# linux
ls，查看当前目录，ll -t，可以按照时间排序，添加 -a 参数，可以查看隐藏文件，有时候出现莫名其妙的 bug 的时候很有用。另外，常用 ls * | wc 命令统计当前目录下面的文件数量，* 表示所有文件，根据实际使用情况可以灵活使用。  
cd，用于切换当前目录，可以是绝对路径，也可以是相对路径，./ 代表当前目录，../ 代表上级目录，cd -，可以切换为上一次使用的目录。  
du，计算目录大小的命令，添加 -h 命令可以按照人们熟悉的 K、M、G 的方式来显示大小。  
cp，文件拷贝，添加 -r 可以拷贝文件夹；mv，文件重名与移动；mv src dst，如果 dst 是文件，则是重命名，如果是目录，则是移动。  
pwd，查看当前路径，这个在移动一些数据集或者整理文件 list 的时候会非常有用。  
locate，find，用于查找某一个文件，具体的参数可以自己去查询。  
rm，删除文件，添加 -r 可以删除目录，该操作要慎用，尤其是注意后面的目录，类似于 sudo rm –rf / 这样的操作，会让你体会到什么叫绝望。  
kill，ps，进程管理相关，常用于批量杀死进程。比如这一条命令，可以杀死所有 caffe 进程：ps -ef | grep caffe | awk '{print $2}' | xargs kill -9。  
tar，unzip 文件解压缩命令。tar –cvf test.tar test 用于压缩，tar –xvf test.tar 用于解压，unzip test.zip 用于解压，zip –r test.zip test 用于压缩，更多内容可自行查阅学习。  
cat，用于显示文件内容及拼接文件。cat test.txt 会将内容显示到终端，cat test1.txt test2.txt >combine.txt，则用于拼接文件。  
chmod，chown：前者用于改变文件权限，后者用于改变文件所有者。  
gcc、g++、cmake、C 语言编译命令，需要额外学习。  
vim ，linux与 Windows 的最大不同是，通常不再使用 IDE，取而代之的是用文本编辑器，其中 VIM 是一个非常优秀而强大的工具，常用的命令有 /test，匹配寻找 test。%s/a/b，替换 a 字符为 b，gg 跳到行首，GG 跳到行尾，dd 删除行，yy 复制行，v 复制范围，Ctrl+V，列编辑模式，更多的内容可以专门开篇学习。  
git，该命令是项目管理必备的，基本命令要熟悉；git clone，拷贝项目；git add，添加文件；git commit，提交修改说明；git push，正式提交代码；git pull，拉取远程代码。  
ssh，远程服务器连接，scp 远程和本地机器文件拷贝。  
Shell 脚本编程，我们经常需要用 Shell 脚本批量处理，所以 Shell 的编程也需要学习。  
--增  
mkdir 创建文件夹  
touch 创建文件  
cp 复制  
--改  
mv 移动  
vi 新建/修改文件  
--删  
rm 删除文件夹
rm -f 删除文件  
--查
cd 进入目录
ls 查看信息
pwd 显示当前路径
find / -name file1 查找/目录下文件 ‘/’表示根目录

# python
* strip  
Python strip() 方法用于移除字符串头尾指定的字符（默认为空格）或字符序列。  
1、strip() 处理的时候，如果不带参数，默认是清除两边的空白符，例如：/n, /r, /t, ' ')。  
2、strip() 带有参数的时候，这个参数可以理解一个要删除的字符的列表，是否会删除的前提是从字符串最开头和最结尾是不是包含要删除的字符，如果有就会继续处理，没有的话是不会删除中间的字符的。  
* ord()  chr()
将字符变为ASCALL码  反变换


# learn_notes

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

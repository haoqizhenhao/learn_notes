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
#from keras.preprocessing import image
img_path = 'images/my_image.jpg'
img = image.load_img(img_path, target_size=(64, 64))
imshow(img)

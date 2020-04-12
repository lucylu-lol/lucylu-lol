# first

**建模流程**

1. 选择模型
2. 构建网络层
3. 编译
4. 训练
5. 预测

```python
(x_train,y_train),(x_test,y_test) = keras.datasets.mnist.load_data()

model = Sequential()

model.add(Conv2D(6,(5,5),input_shape=(32,32,3),activation='relu'))
model.add(MaxPooling2D(pool_size=(2,2)))
model.add(Conov2D(16,(5,5),activation='relu'))
model.add(MaxPooling2D(pool_size=(2,2)))
model.add(Flatten())
model.add(Dense(120,activation='relu'))
model.add(Dense(84,activation='relu'))
model.add(Dense(10,activation='softmax'))

model.fit(x_train,y_train,epochs=5,batch_size=32)
model.predict_classes(x_test)

```


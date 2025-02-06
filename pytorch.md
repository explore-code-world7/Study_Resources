# batch training




# cuda out of memory
0. 按批load to gpu
```py
for batch_idx, batch_data in enumerate(Test_Loader):
    batch_data = batch_data.to(device)
```

对比实验
2. 仅仅将batch_data存储，正常
3. 将神经网络经过模型预测后，无论是否释放模型的输出，都会报错cuda out of memory
* 模型forward的时候保存了计算图,并未清除，可能是这个原因
```py
    gcnet.eval()
    with torch.no_grad():
        pos, _, _, _ = gcnet(batch_data)
```
3. 训练的时候
* first define a optimizer
```py
optimizer = torch.optim.SGD(model.parameters(), lr=learning_rate)
```
* 参数梯度清零
```py
    optimizer.zero_grad()
```
* 参数迭代不计算梯度
```py
    optimizer.step()
```
* [some little stupid but rich functions](https://stackoverflow.com/questions/59129812/how-to-avoid-cuda-out-of-memory-in-pytorch)

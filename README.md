
# 依赖：
```
pip install web3
pip install httpx
```


# 自动打包
右边Releases里打包好的exe是Github Action自动打包

打包脚本[.github/workflows/main.yml](.github/workflows/main.yml)

可以自行Fork仓库，自己去Action→发布软件→Run workflow

等待若干时间，会自动帮你打包好并发布到Releases。


# 使用教程

1. **输入地址**：这是你接收铭文的地址
2. **输入私钥**：这个是小号私钥，放点gas，用完就扔
3. **输入RPC**：打哪个链用哪个链的RPC，有的RPC不支持batchRequest，多换几个
4. **输入maxFeePerGas**：这个是最大gasPrice，可以多给点
5. **输入maxPriorityFeePerGas**：这个是小费gasPrice
6. **输入data**：这个是铭文的十六进制，看别人打的，或者手动点一下，去小狐狸里复制


适用于所有EVM链，所有无编号铭文


**输入的私钥为付gas地址，由于可能卡nonce，请新建个小号，放gas进去，打完转走gas**


一包100个，循环100次，理论上是会跑10000个，但是实际上会卡nonce，多跑几遍就是

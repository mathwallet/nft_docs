本文会手把手教你如何创建一个721标准的 NFT Token

## 编译合约

打开 <https://remix.ethereum.org>

删除默认的文件，新建一个 NFT.sol

从以下仓库中复制合约代码到 NFT.sol

<https://github.com/mathwallet/BSC-Contracts/blob/main/Contracts/NFT.sol>

NFTToken 合约中的构建函数需要做自定义的修改

![](/nft_docs/images/A75F80920F150D40E6C638069B4DFAE2.png)

比如：发一个ColorNFT系列，这个NFT Token叫RED

![](/nft_docs/images/04842D63285FCCB78003DDA95686E6EE.png)

BaseURI 指向一个 meta data 的 URL，具体格式可参考：[http://developer.mathwallet.org/bsc/nfttest/\#](http://developer.mathwallet.org/bsc/nfttest/#)

在这个URL返回的json中，还需要定义该NFT的图片：

<http://developer.mathwallet.org/bsc/nfttest/red.jpg>

该图片需要可访问，这样在钱包以及NFT交易市场中可以直接展示

编译器版本选择 0.5.5

![](/nft_docs/images/8A163F13CDCBADCFFBE7B99B3617D8DC.png)

## 部署合约

![](/nft_docs/images/392931519305D956E16CCD5381956B70.png)

配置合约完成后在Bscscan上完成合约验证，具体步骤见

<http://blog.mathwallet.xyz/?p=4181>

验证完成后，首先使用 addMinter 方法添加一个地址

![](/nft_docs/images/F6D37AD2E1CA6814149B3A4AFC8BBED8.png)

然后即可使用该地址，按序号Mint NFT给任意地址了

![](/nft_docs/images/57DD4F3EA05508C11356BB2A4BD9EE8D.png)

随后就可以在区块浏览器上查看NFT token的信息

[https://testnet.bscscan.com](https://testnet.bscscan.com/token/0x)
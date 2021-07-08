NFT除了链上的唯一性存储在智能合约中，一般还会通过Metadata关联到图片、音乐、视频等文件进行展示，为了实现去中心化的存储，一般会选择使用IPFS协议进行保存。

比如NFT.Storage项目能够让开发者能够利用内容寻址和去中心化存储保护NFT资产及相关元数据——确保所有NFT遵循最佳实践方案并能够长期访问。

NFT.storage凭借IPFS和Filecoin的弹性和持久性，让按照最佳实践铸造NFT变得无比顺畅。

工作原理：

1\. 内容寻址：用户将数据上传至NFT.Storage后，会获得内容的IPFS哈希，也称为CID。CID是数据的独特指纹，无论内容存储发生于何时何地，CID都是指向内容的通用地址。因为CID是基于内容生成，使用它指向NFT数据能预防脆弱连接可能导致的问题以及rug -pull骗局。

2\. 可证明存储：NFT.Storage通过Filecoin实现长期分布式数据存储——对接存储交易和检索交易从而长期保存NFT数据。Filecoin利用密码学证明提供持久协议层来保障NFT数据的持久性和耐用性。

3\. 弹性检索：利用IPFS和Filecoin存储的数据可轻松获取，只需用浏览器打开任意公共IPFS端口。

![](/nft_docs/images/C8E8B9247E689ABA6EB41B59F328D4D6.png)

# 部署元数据 API

您可以将其托管在 IPFS、云存储或您自己的服务器上。为了让您开始，我们在 Python 和 NodeJS 中创建了一个示例 API 服务器：

[Python 示例 API 服务器](https://github.com/ProjectOpenSea/metadata-api-python)

[NodeJS 示例 API 服务器](https://github.com/ProjectOpenSea/metadata-api-nodejs)

如果您使用[IPFS](https://ipfs.io/)来托管您的元数据，您的URL应该是 `ipfs://\<hash\>`. 

例如，`ipfs://QmTy8w65yBXgyfG2ZBg5TrfB2hPjrDQH3RCQFJGkARStJb`。如果您打算存储在 IPFS 上，我们建议使用[Pinata](https://pinata.cloud/)来轻松存储数据。

[Arweave](https://www.arweave.org/)的对等的是 `ar://\<hash\>` 例如`ar://jK9sR4OrYvODj7PD3czIAyNJalub0-vdV\_JAg1NqQ-o`。

Freezing Metadata

您可以通过从智能合约发出此事件来向 OpenSea 表明 NFT 的元数据不再被任何人更改（换句话说，它已“冻结”）

event PermanentURI(string \_value, uint256 indexed \_id);
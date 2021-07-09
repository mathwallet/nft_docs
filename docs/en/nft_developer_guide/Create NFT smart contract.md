This article will teach you how to create a 721 standard NFT Token.

### Compile the Smart contract

Open <https://remix.ethereum.org>

Delete the default file and create a new NFT.sol

Copy the contract code from the following warehouse to NFT.sol

<https://github.com/mathwallet/BSC-Contracts/blob/main/Contracts/NFT.sol>

The construction function in the NFTToken contract needs to be customized.

![](/nft_docs/images/A75F80920F150D40E6C638069B4DFAE2.png)

For example: create a ColorNFT series, this NFT token is called RED

![](/nft_docs/images/04842D63285FCCB78003DDA95686E6EE.png)

BaseURI points to a meta data URL, the specific format can be referred to: [http://developer.mathwallet.org/bsc/nfttest/\#](http://developer.mathwallet.org/bsc/nfttest/#)In the json returned by this URL, the image of the NFT also needs to be defined:

<http://developer.mathwallet.org/bsc/nfttest/red.jpg>

The picture needs to be accessible so that it can be displayed directly in the wallet and NFT trading market

Compiler version selection 0.5.5

![](/nft_docs/images/8A163F13CDCBADCFFBE7B99B3617D8DC.png)

## Deployment contract

![](/nft_docs/images/392931519305D956E16CCD5381956B70.png)

After configuring the contract, complete the contract verification on Bscscan, see the specific steps<http://blog.mathwallet.xyz/?p=4181>

After verification is complete, first use the addMinter method to add an address

![](/nft_docs/images/F6D37AD2E1CA6814149B3A4AFC8BBED8.png)

Then you can use the address, give any address according to the serial number Mint NFT

然后即可使用该地址，按序号Mint NFT给任意地址了

![](/nft_docs/images/57DD4F3EA05508C11356BB2A4BD9EE8D.png)

Then you can view the NFT token information on the block explorer

<https://testnet.bscscan.com>
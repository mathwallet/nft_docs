**NFT standard**

****

The NFT standard is what makes non-homogeneous assets outstanding. It assures the developer that the asset will behave in a certain way and describe exactly how it interacts with the basic functionality of the asset.

Ethereum's ERC721 and ERC1155 standards are currently widely used. In addition to Ethereum, some Ethereum compatible public chains also use this standard, such as BSC, HECO, Polygon, etc.

**ERC721**

ERC721, initiated by CryptoKitties, is the first standard to represent non-homogeneous digital assets. ERC721 is an inheritable smart contract standard, which means developers can easily import it to create a new OpenZeppelin library that is consistent with the ERC721-contract (here we create our first useful tutorial on the ERC721 contract). ERC721 is actually pretty simple: It provides a mapping of a unique identifier (each identifier represents an asset) to an address that represents the owner of the identifier. ERC721 also provides permission to transfer assets using the transferFrom method.

If you think about it, these two approaches are really all you need to represent NFT: one is to check who has what, and the other is to send what. The standard has few other features (some of which are important to the NFT market), but the core of ERC721 is very basic.

See details: [https://github.com/ethereum/EIPs/blob/master/EIPS/eip-721.md](about:blank)

**ERC1155**

ERC1155, innovated by the Enjin team, proposes a semi-homogeneous solution for the NFT world. In ERC1155, the ID does not represent the asset, but the class of the asset. For example, an ID might represent a "sword," and a wallet might have 1,000 of these swords. In this case, the balance O method will return the number of swords owned by the wallet, and the user can transfer any number of these swords by calling "sword ID" through transferFrom.

Analysis of ERC20, ERC721, ERC1155 standards. ERC20 maps addresses to amounts, ERC721 maps unique IDs to owners, and ERC1155 has nested mappings that map IDs to owners and quantities.

See details: [https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1155.md](about:blank)

**Non-Ethereum standards**

Although Ethereum is currently the foundation for most of the NFT projects, several other NFT standards have emerged onto other chains. Dgoods is a pioneer of the Mythical Gaming team, which has been working on a functional cross-chain standard since EOS. The projects on Cosmos are also developing the NFT module, which is available as part of the Cosmos SDK. The NFT standard represented by RMRK is currently available on Polkadot's canary network Kusama.
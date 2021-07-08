元数据也叫 Metadata。

每个NFT通证都会有一个自己的Metadata URI，它是一个json格式的文本，里面定义了NFT一些更详细的信息，比如NFT的名称、描述、图片的URL以及特殊属性等。

我们建议开发者按照ETH标准的定义来设置URI结构，这样能够方便NFT交易平台（如Opensea）、去中心化钱包（如MathWallet）能够对该NFT进行支持和展示。

标准文档

<https://github.com/ethereum/EIPs/pull/1028>

Sample

<https://gist.githubusercontent.com/jamesmorgan/7599542b6aeb226f45daf661e82d3e70/raw/e175228c3cf1eefee6d633880de6fe6a8951d251/erc-721-enhanced-metadata.json>

image:这是项目图像的 URL。几乎可以是任何类型的图像（包括 SVG，甚至是 MP4），并且可以是IPFS URL 或路径。

image\_data: 原始 SVG 图像数据，仅当您不包含 image 参数时才使用它。

external\_url: 将允许用户跳转至该网页上查看该项目

description: 人类可读的描述，支持Markdown格式。

name: NFT的名称

attributes:NFT的属性

background\_color:项目的背景颜色，\#开头的十六进制字符。

animation\_url:项目多媒体附件的 URL。支持文件扩展名 GLTF、GLB、WEBM、MP4、M4V、OGV 和 OGG，以及仅音频扩展名 MP3、WAV 和 OGA。Animation\_url 还支持 HTML 页面，允许您使用 JavaScript 画布、WebGL 等构建丰富的体验和交互式 NFT。现在支持 HTML 页面中的脚本和相对路径。但是，不支持访问浏览器扩展。

youtube\_url:YouTube 视频的 URL。
# BNX Token(新)

## 合约地址：0xb3a6381070B1a15169DEA646166EC0699fDAeA79

## 合约状态：开源

## 合约属性：BEP-20 Token

## 创建时间：Aug-24-2021 10:13:37 AM +UTC

## 创建哈希：0x20a381ed1c08177ba5ae09fc8e1d3991067f81dcc521ce5af7dddc3ccb2da506

## 合约创建者：0x1221979949248eb2132720c173212d327f0d389b

## 编译器版本：v0.6.12+commit.27d51765

## 总供应量：73758083649.589559812052375677

## 合约创建者手续费来源：

* 交易哈希: 0x07c73a3971a6b93342d605c570f27cd29db110870d2604efaf03a591268d4fee 

  来源地址: 0xeb2d2f1b8c558a40207669291fda468e50c8a0bb (Binance: Hot Wallet 10)

* 交易哈希: 0x3bab7d3d5966674d0bd39f76fc2982aa419d6f39a31ab5c06c8f714fc19f640c 

  来源地址: 0x2b5d06E2b65Ae5b2f8684E8196E2B94cc60B0736

* 交易哈希: 0x905f25adfe9d89620469e0a760391c07e74d32693df468fa50229c8a22a6ff85 

  来源地址: 0x80DFCe00b7E272F189a4366595082cA90e9fa146

* 交易哈希: 0x82a4a8e968c4ba5d94b73d6157e850fa4a90a6b9865b9bece44f96be09b0c440 

  来源地址: 0x2D08dfA7bc304f203Ed22812a3997855e197655a

## Dex 池子大小：
    ### pancakeswap:
        (0xc2f1A40D3ba746B913C798057d8010800AAce255) value:1143449 BUSD
        dex中 pancakeswap 占有 0.2196% 的代币总流通量，排名第82。除去黑洞地址外，拥有 10% 以上 pancakeswap 代币量的 EOA 和地址总数约为 14，拥有 50% 以上 pancakeswap 代币量的 EOA 和地址总数约为 4，拥有 100% 以上 pancakeswap 代币量的 EOA 和地址总数约为 2

## 分析：

1. 合约有黑名单功能，能冻结地址余额
2. 合约的 owner 没有被舍弃，当前的 owner 地址为 0x1221979949248eb2132720c173212d327f0d389b(owner和合约创建者为同一地址)
3. 合约的 owner 拥有 mint 和管理黑名单的权限，能够进行增发代币和冻结代币，并授权其他地址进行代币增发

## 风险：

1. 当前合约属于中心化合约， owner 能够控制代币的增发，进而在 dex 上进行砸盘
2. 大约 10 个 EOA 或者合约有能力对 dex 中代币的价格造成显著的影响
3. 合约所使用的编译器版本小于 0.8.0，存在整数溢出漏洞的可能性

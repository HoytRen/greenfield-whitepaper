# Greenfield白皮书

BNB Greenfield的目标是释放去中心化区块链和存储技术在数据所有权和数据经济方面的力量。

BNB Greenfield不仅是BNB中的新区块链，还是一个基础设施和生态系统，旨在促进去中心化数据经济。 它通过简化存储和管理数据访问的流程，并将数据所有权与BSC的大规模DeFi环境联系起来，来实现这一目标。

它致力于与现有的中心化和去中心化存储系统不同的三点：

- 它使以太坊兼容地址能够创建和管理数据和代币资产。

- 它以可交换的资产和智能合约程序的形式，将数据权限和管理逻辑本地化地与BSC上的其他资产连接起来。

- 它为开发者提供与现有流行的Web2云存储类似的API基本概念和性能。

我们期待Greenfield能建立一个新的数据经济和dApp模型的试验场和测试场，并最终成为Web3基础设施的一部分。

这个代码库中的白皮书描述了该平台的主要设计和实现。 许多想法都基于其他先锋协议和团队的巨大贡献。 请参考致谢章节。

我们欢迎任何建设性的意见、想法和反馈。

希望每个人都能享受这个旅程！

## 目录

- [概述](./overview.md)
- [第一部分 BNB Greenfield和去中心化存储经济的设计](./part1.md)
  - [1 设计原则](./part1.md#1-design-principles)
  - [2 假设](./part1.md#2-assumptions)
  - [3 总体架构](./part1.md#3-the-architecture-in-general)
    - [3.1 Greenfield的核心](./part1.md#31-greenfield-core)
    - [3.2 BNB Greenfield dApps](./part1.md#32-bnb-greenfield-dapps)
    - [3.3 与BSC的交互](./part1.md#33-the-cross-chain-with-bsc)
    - [3.4 三方受益](./part1.md#34-the-trinity)
  - [4 BNB Greenfield的核心](./part1.md#4-bnb-greenfield-core)
    - [4.1 BNB Greenfield区块链](./part1.md#41-the-bnb-greenfield-blockchain)
    - [4.2 存储提供者：SP](./part1.md#42-the-storage-providers-sps)
    - [4.3 相互配合](./part1.md#43-the-pair-synergy)
  - [5 Greenfield数据存储](./part1.md#5-the-greenfield-data-storage)
    - [5.1 与共识有关的数据](./part1.md#51-data-with-consensus)
      - [5.1.1 账户和余额](./part1.md#511-accounts-and-balance)
      - [5.1.2 验证器和SP元数据](./part1.md#512-validator-and-sp-metadata)
      - [5.1.3 存储元数据](./part1.md#513-storage-metadata)
      - [5.1.4 权限元数据](./part1.md#514-permission-metadata)
      - [5.1.5 计费元数据](./part1.md#515-billing-metadata)
    - [5.2 载荷对象数据的离线存储](./part1.md#52-off-chain-payload-object-data-storage)
      - [5.2.1 主要和辅助SP](./part1.md#521-primary-and-secondary-sps)
      - [5.2.2 数据冗余](./part1.md#522-data-redundancy)
  - [6 存储经济及其基本概念](./part1.md#6-storage-economics-and-its-primitives)
    - [6.1 创建账户](./part1.md#61-account-creation)
    - [6.2 创建数据对象](./part1.md#62-data-object-creation)
    - [6.3 数据存储](./part1.md#63-data-storage)
    - [6.4 读取数据和下载](./part1.md#64-data-read-and-download)
    - [6.5 权限和权限组](./part1.md#65-permissions-and-group)
    - [6.6 费用和支付方式](./part1.md#66-fees-and-payments)
    - [6.7 数据完整性和可用性挑战](./part1.md#67-data-integrity-and-availability-challenge)
    - [6.8 删除数据](./part1.md#68-data-delete)
  - [7 数据资产经济学](./part1.md#7-economy-of-data-assets)
    - [7.1 与BSC的交互](./part1.md#71-cross-chain-with-bsc)
    - [7.2 框架](./part1.md#72-framework)
    - [7.3 通信层](./part1.md#73-communication-layer)
    - [7.4 资源副本层](./part1.md#74-resource-mirror-layer)
      - [7.4.1 资源实体的副本](./part1.md#741-resource-entity-mirror)
      - [7.4.2 跨链操作的基本概念](./part1.md#742-cross-chain-operating-primitives)
  - [8 设计“没有”结束](./part1.md#8-not-ending-for-the-design)
    - [8.1 致谢](./part1.md#81-acknowledgement)
- [第二部分 试验中的使用场景](./part2.md)
  - [9 场景：去中心化存储](./part2.md#9-showcases-decentralized-storage)
    - [9.1 网站托管和个人云盘](./part2.md#91-web-hosting-and-personal-cloud-drive)
    - [9.2 公链的数据可用性层](./part2.md#92-data-availability-layer-for-public-blockchain)
      - [9.2.1 一层链的数据交换](./part2.md#921-layer-1-blockchain-data-swapping)
      - [9.2.2 在二层的Rollup的数据可用性层](./part2.md#922-data-availability-layer-for-the-layer-2-rollups)
      - [9.2.3 快照和块数据备份](./part2.md#923-snapshots-and-block-data-backups)
  - [10 场景：数字出版的新形式](./part2.md#10-showcases-new-ways-of-digital-publishing)
    - [10.1 草根数字出版](./part2.md#101-grass-root-digital-publishing)
    - [10.2 数据市场](./part2.md#102-data-market)
    - [10.3 风险：反盗版](./part2.md#103-risk-anti-piracy)
  - [11 场景：用户生成内容](./part2.md#11-showcases-user-generated-content)
    - [11.1 反垄断和反掩盖](./part2.md#111-anti-monopoly-and-anti-censorship)
    - [11.2 通过代币推举的榜单](./part2.md#112-token-curated-registries)
  - [12 场景：个人数据市场](./part2.md#12-showcases-personal-data-market)
  - [13 从场景到落地](./part2.md#13-from-showcases-to-real-production)
- [第三部分 技术规格简述](./part3.md)
  - [14 生态系统组成](./part3.md#14-ecosystem-players)
    - [14.1 Greenfield验证器](./part3.md#141-greenfield-validators)
    - [14.2 存储提供器（SP）](./part3.md#142-storage-providers-sps)
    - [14.3 Greenfield dApps](./part3.md#143-greenfield-dapps)
  - [15 用户标识符](./part3.md#15-user-identifier)
    - [15.1 用户余额](./part3.md#151-user-balance)
  - [16 Greenfield区块链](./part3.md#16-greenfield-blockchain)
    - [16.1 代币经济学](./part3.md#161-token-economics)
    - [16.2 共识及验证器的选举](./part3.md#162-consensus-and-validator-election)
    - [16.3 治理交易](./part3.md#163-governance-transactions)
      - [16.3.1 创建和设置验证器](./part3.md#163-governance-transactions)
      - [16.3.2 抵押奖励的分配](./part3.md#1632-staking-reward-distributio-n)
      - [16.3.3 创建存储提供器](./part3.md#1633-create-storage-provider)
      - [16.3.4 移除存储提供器](./part3.md#1634-remove-storage-provider)
  - [17 存储元数据模型](./part3.md#17-storage-metadata-models)
    - [17.1 桶](./part3.md#171-bucket)
    - [17.2 对象](./part3.md#172-object)
    - [17.3 组](./part3.md#173-group)
    - [17.4 权限](./part3.md#174-permission)
      - [17.4.1 所有权](./part3.md#1741-ownership)
      - [17.4.2 定义权限](./part3.md#1742-permission-definitions)
      - [17.4.3 移除权限](./part3.md#1743-permission-removal)
      - [17.4.4 示例](./part3.md#1744-examples)
  - [18 载荷存储管理](./part3.md#18-payload-storage-management)
    - [18.1 片段](./part3.md#181-segments)
    - [18.2 纠删码和数据冗余](./part3.md#182-erasure-code-and-data-redundancy)
      - [18.2.1 数据冗余设计](./part3.md#1821-data-redundancy-design)
      - [18.2.2 纠删码](./part3.md#1822-erasure-code)
        - [18.2.2.1 编码](./part3.md#18221-encoding)
        - [18.2.2.2 解码：数据恢复](./part3.md#18222-decoding-data-recovery)
  - [19 数据可用性挑战](./part3.md#19-data-availability-challenge)
    - [19.1 初始数据完整性和冗余元数据](./part3.md#191-the-initial-data-integrity-and-redundancy-metadata)
    - [19.2 数据可用性挑战流程](./part3.md#192-data-availability-challenge-process)
  - [20 存储交易](./part3.md#20-storage-transactions)
  - [21 计费和支付](./part3.md#21-billing-and-payment)
    - [21.1 概念和公式](./part3.md#211-concepts-and-formulas)
      - [21.1.1 术语](./part3.md#2111-terminology)
      - [21.1.2 公式](./part3.md#2112-formula)
      - [21.1.3 类型和接口](./part3.md#2113-types-and-interfaces)
    - [21.2 关键工作流程](./part3.md#212-key-workflow)
      - [21.2.1 抵押和提币](./part3.md#2121-deposit-and-withdrawal)
      - [21.2.2 流式支付](./part3.md#2122-payment-stream)
      - [21.2.3 强制结算](./part3.md#2123-forced-settlement)
      - [21.2.4 支付账户](./part3.md#2124-payment-account)
      - [21.2.5 账户冻结和恢复](./part3.md#2125-account-freeze-and-resume)
      - [21.2.6 存储费用计价和调整](./part3.md#2126-storage-fee-price-and-adjustment)
  - [22 跨链模型](./part3.md#22-cross-chain-models)
    - [22.1 通信通道和数据包](./part3.md#221-communication-channels-and-packages)
      - [22.1.1 投票调查](./part3.md#2211-vote-poll)
      - [22.1.2 通道和序列](./part3.md#2212-channel-and-sequence)
      - [22.1.3 可靠性协议](./part3.md#2213-reliability-protocol)
      - [22.1.4 验证器的更新](./part3.md#2214-validator-update)
    - [22.2 经济学](./part3.md#22-2-economic)
      - [22.2.1 跨链数据包的费用和奖励](./part3.md#2221-fee-and-reward-of-cross-chain-packages)
      - [22.2.2 跨链数据包的交付竞争](./part3.md#2222-race-to-deliver-cross-chain-packages)
      - [22.2.3 回调和Gas限制](./part3.md#2223-callbacks-and-limited-gas)
      - [22.2.4 BSC上的跨链基础设施合约](./part3.md#2224-cross-chain-infrastructure-contracts-on-bsc)
    - [22.3 错误和失败的处理](./part3.md#223-error-and-failure-handling)
  - [23 SP API](./part3.md#23-sp-apis)
    - [23.1 通用终端](./part3.md#231-universal-endpoint)
      - [23.1.1 URI标准](./part3.md#2311-uri-standard)
      - [23.1.2 HTTPS REST API](./part3.md#2312-https-rest-api)
      - [23.1.3 P2P RPC](./part3.md#2313-p2p-rpc)
    - [23.2 和“列出”有关的操作](./part3.md#232-list-operations)
- [总结](./ending.md)

## 参与贡献

1. 复制代码库并切换到一个分支

  ```shell
  git clone https://github.com/bnb-chain/greenfield-whitepaper.git
  git checkout -b <your-branch-name>
  ```

2. 进行修改

3. PR之前先检查文件格式

  ```shell
  # install markdownlint-cli from https://github.com/igorshubovych/markdownlint-cli
  markdownlint '**/*.md'  -c .github/workflows/markdownlint.yaml
  ```

4. 提交PR

## 许可协议

所有内容均依据 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)授权。

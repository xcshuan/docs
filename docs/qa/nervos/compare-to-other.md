---
id: compare-to-other
title: Nervos 如何在众多公链中脱颖而出
sidebar_label: Nervos 如何脱颖而出
---

关于 Nervos 如何在众多公链项目中脱颖而出，我觉得这是结果。Nervos CKB 跟绝大部分公链项目完全不同，走的是一条不一样的路，所以 Nervos 实际上已经非常不同了。

### 关于扩容

众多较新推出的公链为了实现扩展性，提出通过分片的链上扩容，或者多链扩容的路线，我们认为链上扩容始终需要面对跨片安全性的挑战，并且不认同牺牲一定的安全性换取更低得交易成本。而在多链模式下，我们走的是分层架构解决扩展性问题的路线，通过 Layer 2 构建丰富得应用层，通过 Layer 2 来获得近乎无限的扩展性。

### 关于共识

众多较新推出得公链为了追求共识性能，在安全和去中心化方面做妥协，比如选择 PoS 共识算法，并为此大搞节点竞选。而 Nervos 依然选择 PoW，并且开发出了在中本聪 Nakamoto 共识基础上的改进共识协议 NC-Max。拥有更高吞吐量的同时，在安全和去中心化方面跟中本聪共识一样不做哪怕一丝一毫得妥协，这事因为我们认为底层的核心是安全和资产保管，并且捕获时间积累带来的信任价值，这一点唯有坚持 PoW 才能做到。

### 关于虚拟机

众多较新推出得公链选择兼容 EVM 或者 EVM 的下一代虚拟机 WebAssembly，方便把以太坊上的存量生态直接朝着自己的链上搬，然后 EVM，包括 WebAssembly 虚拟机受限于架构和自身设计，无法做到灵活有效的扩展去支持多种多样的密码学算法，我们基于 RISC-V 开发的虚拟机 CKB-VM，从底层设计上更加灵活，可以任意添加自定义密码学原语支持，这种灵活性能真正释放区块链潜力，尤其是在跨链和互操作性方面优势特别明显，以及能非常方便的构建基于 CKB 之上的二层应用扩展，并方便第三方任意链跨链到 CKB。

### 关于资产

众多较新推出得公链选择支持智能合约，通过智能合约发行和管理资产，殊不知这里其实存在很多问题，最大的问题是智能合约是被系统第一优先级支持，还是资产被第一优先级支持，两个出发点不同，结果完全不同。我们提出了 [FCA（First Class Asset）](https://talk.nervos.org/t/first-class-asset/405)即把资产作为第一等公民有限支持，直接提供编程能力操作和引用，而非把智能合约作为一等公民，避免通过智能合约去操作资产带来的各种不方便和不经济的问题。这种智能合约为资产服务，而不是资产为智能合约服务得编程范式层面的变革，在我们眼里才是回归本源和面向未来，在 Nervos CKB 提出 FCA 一年多后，我们欣喜得看到 Facebook 的 Libra，提出一套编程范式叫做面向资源编程，跟 Nervos 提出的 FCA 非常接近，这更让我们印证了 FCA 是面向未来的方向。

### 关于经济模型

众多较新推出得公链在经济模型设计的时候，偏向选择当下市场的趋势和喜好来设计经济模型和货币政策，而 Nervos 在设计经济模型的时候核心之关注三点：保障系统安全，公平以及可持续。公平性提现在利益对其，不同角色的参与者，每个人对网络的贡献和拿到的激励对齐，并且规则清晰目标明确，只有在规则透明且公平的系统中，参与者才有意愿投入做出更多的贡献，这个道理就像分蛋糕，当分配规则公平透明，每个人能分到的蛋糕取决于大家能一起把蛋糕做多大。可持续性提现在我们 fix 了比特币经济模型中一个影响长期可持续性的 bug，并且提出了一整套价值捕获理论，这在整个行业是开先河之举。


### 关于跨链

关于跨链，有两个方向，一个方向 Nervos Network 的 CKB 层和 Layer 2 层之间的跨链，在 Nervos 发布的 2020 Roadmap 中，排第一位的重头项目 Muta 框架是一个高性能的区块链框架，对标的项目是 Cosmos SDK 和 Polkadot 的 Substrate，开发者可以根据需求基于 Muta 定制开发一条链，Muta 和 CKB 之间的互操作性，可以让任何采用 Muta 框架的区块链都能和 CKB 进行跨链交互，一个真实的案例是 Nervos 基金会与火币集团合作开发的火币公链，就是基于 Muta 框架开发的监管友好的金融公链。

另外一个方向是其他公链比如 Bitcoin，Ethereum 等跨链到 Nervos CKB，在我们已经宣布的 Grants 项目的第一个审核通过的项目 [bitcoin-spv for CKB](https://talk.nervos.org/t/grant-rfc-bitcoin-spv-utils/4162) 实现了一套组件和工具库可以把 Bitcoin 跨到 CKB 上，我们希望通过 Grants 的方式跟开发者社区合作，由开发者社区来实现各种跨链基础设施类项目。
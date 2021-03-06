## 0x00 论文基本信息

我阅读的这篇文章题目是《Smart Meter Data Obfuscation Using Correlated Noise》，从性质上来说算是一篇阐述技术的文章,作者分别是A. S. Khwaja, A. Anpalagan, M. Naeem, and B. Venkatesh。它出自期刊

```
《IEEE Internet of Things Journal》
```

## 0x01 论文主要内容

在论文中，作者主要提出了一种基于加噪声的智能电表数据的数据混淆技术。这个噪声用于掩盖不同用户传输给第三方的数据，从而防止窃听。但是对于合法接收者，他们又可以准确恢复出原始数据的统计信息。该篇论文通过模糊测试混淆的强度和检查恢复数据的准确性这两个方面来对整个混淆技术进行评估，并且利用了深度学习技术证明这种情况下的性能。

## 0x02 论文主要优点和创新点

这篇论文的主要创新点非常明显，对于数据的混淆是之前的研究没有注重的。往常的研究都是基于对数据的加密，例如生成密钥对并分发，另一方面，该研究引入了深度学习技术，阐述了自动化的混淆和分析。由于论文涉及太多的专业知识和数学计算，我无法完全摸清其中的细节，但是从实验图表中就可以看到，混淆效果是比较成功的。


## 0x03 论文缺点

从篇章建构来看，该篇论文的部分布局结构有改善空间。作者在开篇就阐述一般放在总结部分的related work， 没有开门见山地直入主题。另一方面，该技术有着比较高的要求，例如硬件设备需要是低成本的。

## 0x04 其他替代方案与改进方法

首先，就该技术的目的来看，它是为了防止原始数据信息在传输过程中被窃听而被提出的，那么根据这个目的可以提出替代方案。
第一种替代方案就是常规的对数据进行加密。通信的双方首先进行密钥协商，然后在传输数据的时候发送方使用密钥进行加密，接收方在接收端解密出原始的数据统计信息。
第二种替代方案是使用更安全可靠的信道来传输源数据。
第三种替代方案是类似于二进制安全中的Canary技术，在传输过程中设置某种哨兵，能够探测到周围的窃听，一旦发现窃听，就立刻停止传输并报警。
关于文章建构的改进，我认为需要将related work 部分放置在文章偏后部分阐述。

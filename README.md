# FilecoinCash 公告
[English version](#FilecoinCash-Notice)

很高兴FilecoinCash社区在9月18日正式成立，将于9月19日晚些时候开放Github代码库，前期出于保护项目的考虑，测试阶段只会开放部分源代码，在主网上线前开源全部代码。
#### 19日发布的[第一个版本](https://github.com/filecoincash/lotus/releases/tag/v0.5.7-beta) ，做了如下改进：
- 封装修改为4G版本。
- P1部分封装层数修改为5层。

这两项改进将大幅降低内存使用量，降低参与门槛。

同时，今天会发布sha512算法的测试版执行文件，矿工可使用该执行文件测试设备性能。 

[bench-beta](https://github.com/filecoincash/filecoincash_doc/releases/tag/benchy-sha512-beta) 

使用方法参考：https://github.com/filecoincash/filecoincash_doc/bench/

> bench.sh
```
nohup env FIL_PROOFS_USE_GPU_COLUMN_BUILDER=1 FIL_PROOFS_USE_GPU_TREE_BUILDER=1 RUST_LOG=info ./benchy prodbench --config config.json > log-bench.log 2>&1 &
```

> config.json
```
{
	"sector_size" : "4294967296",
	"porep_challenges" : 2,
	"porep_partitions" : 1,
	"post_challenges" : 20,
	"post_challenged_nodes" : 2,
	"stacked_layers" : 3,
	"num_sectors" : 1
}
```

社区宣布成立后，经过大量社区意见沟通，大部分矿工提议希望给一些测试时间，预先准备好设备测试之后再开启测试奖励网，在此期间会与社区及矿工进行充分沟通，制定一份符合社区及矿工期望的测试奖励网规则。


#### 在下一个版本里，将会有更大的更新：

- 封装修改为4G和16G版本。
- sha256算法修改为sha512算法，在sha512算法下，AMD处理器与Intel处理器有相同的竞争力。
- 发起FilecoinCash初版经济模型提案。
- 发布测试奖励网细则，并确认测试奖励网开启时间。

此版本仅为测试、意见收集版，非最终版本。

FilecoinCash致力于构建更开放的IPFS存储网络。

# 

# FilecoinCash Notice

[中文版本](#FilecoinCash-公告)

I'm very glad that the FilecoinCash community was officially established on September 18, and the GitHub code base will be opened later on September 19. In the early stage, for the sake of protecting the project, only part of the source code will be opened in the test phase, and all the code will be opened before the main network goes online.

#### [The first version](https://github.com/filecoincash/lotus/releases/tag/v0.5.7-beta) released on the 19th made the following improvements:  

- The package was modified to 4G versions.

- The number of package layers in P1 is changed to 5.

These two improvements will significantly reduce memory usage and reduce the threshold of participation.
At the same time, the test version of SHA512 will be released today, which can be used by miners to test equipment performance.

[bench-beta](https://github.com/filecoincash/filecoincash_doc/releases/tag/benchy-sha512-beta) 

Use method reference: https://github.com/filecoincash/filecoincash_doc/bench/

> bench.sh
```
nohup env FIL_PROOFS_USE_GPU_COLUMN_BUILDER=1 FIL_PROOFS_USE_GPU_TREE_BUILDER=1 RUST_LOG=info ./benchy prodbench --config config.json > log-bench.log 2>&1 &
```

> config.json
```
{
	"sector_size" : "4294967296",
	"porep_challenges" : 2,
	"porep_partitions" : 1,
	"post_challenges" : 20,
	"post_challenged_nodes" : 2,
	"stacked_layers" : 3,
	"num_sectors" : 1
}
```

After the establishment of the community, after a large number of community opinion communication, most miners proposed to give some testing time, prepare equipment test in advance, and then open the test reward network. During this period, they will fully communicate with the community and miners, and formulate a test reward network rules that meet the expectations of the community and miners.

#### In the next release, there will be a bigger update:

- The package was modified to 4G and 16g versions.

- Sha256 algorithm is modified to SHA512 algorithm. Under SHA512 algorithm, AMD processor has the same competitiveness as Intel processor.

- The first version of the economic model proposal of FilecoinCash was launched.

- Release the detailed rules of the test reward network and confirm the opening time of the test reward network.

This version is only a test and opinion gathering version, not the final version.

FilecoinCash is committed to building a more open IPFs storage network.
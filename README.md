# Reference_Survey_20261026MON-public
Reference_Survey_20261026MON-public



## Reference_Survey_20261026MON_083642

<box gap={3}> <row align=start gap={3}> <box flex="1" gap={1}> <text weight="medium">1. <Link url="https://arxiv.org/abs/2003.12197" title="HERS: Homomorphically Encrypted Representation Search"/></text> <caption>Engelsma et al., 2022</caption> 暗号化した画像特徴ベクトルを対象に、大規模な類似検索を実現する研究。1億件規模の実験が報告されています。かなり重要な先行研究です。<Cite ref="turn166671search0"/> </box> <badge color="success">重要</badge> </row> <divider color="subtle"/> <box gap={1}> \*\*2. <Link url="https://arxiv.org/abs/2608.21131" title="Billion-Scale Nearest-Neighbor Search under Fully Homomorphic Encryption on a Single GPU"/>\*\*

<caption>Isozaki et al., 2026年8月</caption> 10億件規模のベクトル検索を扱っています。次元削減と階層構造を利用する発想が、以前検討したクラスタリング方式と近いですね。ただしアクセスパターンからの情報漏洩も問題としています。<Cite ref="turn166671academia35"/> </box> <divider color="subtle"/> <box gap={1}> \*\*3. <Link url="https://link.springer.com/article/10.1007/s12083-026-02267-x" title="Single-server CPA-secure and post-quantum encrypted kNN queries"/>\*\*

<caption>2026年</caption> CKKS による暗号化ソートと Top-k 選択を扱っています。われわれが気にしていた比較演算や指示関数の多項式近似と直接関係しそうです。<Cite ref="turn482256search10"/> </box> <divider color="subtle"/> <box gap={1}> \*\*4. <Link url="https://eprint.iacr.org/2024/1894" title="A non-comparison oblivious sort and its application to private k-NN"/>\*\*

<caption>Azogagh et al., 2024</caption> TFHE の LUT を利用した、比較演算に依存しない暗号化 Top-k 選択。CKKS とは方式が違いますが、代替案として興味深い論文です。<Cite ref="turn482256search9"/> </box> <divider color="subtle"/> <box gap={1}> \*\*5. <Link url="https://www.usenix.org/conference/usenixsecurity25/presentation/bian" title="Engorgio: An Arbitrary-Precision Unbounded-Size Hybrid Encrypted Database via Quantized Fully Homomorphic Encryption"/>\*\*

<caption>USENIX Security 2025</caption> 暗号化ベクトル検索とリレーショナルデータ検索を統合するシステム。比較・並べ替えの処理が参考になりそうです。<Cite ref="turn482256search13"/> </box> </box>



### 1\. 入門・サーベイ

最初の2件がおすすめ。

1\. [Homomorphic Encryption for Machine Learning Applications with CKKS Algorithms: A Survey of Developments and Applications](https://www.techscience.com/cmc/v85n1/63510/html?utm_source=chatgpt.com)

Wu et al. (2025) · サーベイ · オープンアクセス

CKKS を中心に、KNN、K-means、顔認識への応用を整理。今回の調査の出発点に向いています。

最優先

2\. [Approximate homomorphic encryption based privacy-preserving machine learning: a survey](https://link.springer.com/article/10.1007/s10462-024-11076-8?utm_source=chatgpt.com)

Artificial Intelligence Review (2025) · サーベイ · オープンアクセス

近似準同型暗号とプライバシー保護機械学習の全体像を整理しています。

3\. [From accuracy to approximation: A survey on approximate homomorphic encryption and its applications](https://www.sciencedirect.com/science/article/pii/S157401372400073X?utm_source=chatgpt.com)

Computer Science Review (2025) · サーベイ

近似準同型暗号の技術と応用を広く扱った総説。

4\. [Fully Homomorphic Encryption for Privacy-Preserving Machine Learning Using the OpenFHE Library](https://openfheorg.github.io/aaai-2024-lab-materials/?utm_source=chatgpt.com)

AAAI 2024 · チュートリアル

OpenFHE の公式教材。CKKS と Python による実験を含むので、現在の環境とも直結します。

5\. [Bootstrapping in approximate fully homomorphic encryption: a research survey](https://link.springer.com/article/10.1186/s42400-025-00384-3?utm_source=chatgpt.com)

2025 · サーベイ

CKKS の bootstrapping に関する総説。HERS など暗号化検索の応用にも触れています。

### 2\. 関連論文

こちらは、タイトルと年代、それに簡単な説明だけにしておきます。

| 年    | 論文・資料                                                                                                                  |
| ---- | ---------------------------------------------------------------------------------------------------------------------- |
| 2022 | HERS: Homomorphically Encrypted Representation Search — 暗号化された特徴ベクトルの大規模検索                                             |
| 2024 | A non-comparison oblivious sort and its application to private k-NN — TFHE と Top-k 選択                                  |
| 2024 | FPGA-Based Acceleration of K-Nearest Neighbor Algorithm on Fully Homomorphic Encrypted Data — CKKS を使った kNN の高速化       |
| 2025 | Privacy-Preserving Approximate Nearest Neighbor Search on High-Dimensional Data — 高次元 ANN、専用の暗号方式                      |
| 2025 | VeriKNN: A verifiable and efficient secure k-NN query scheme — 準同型暗号と2クラウド構成                                           |
| 2026 | Privacy-Preserving Product-Quantized Approximate Nearest Neighbor Search Framework — FHE、TEE、Product Quantization の組合せ |
| 2026 | Billion-Scale Nearest-Neighbor Search under Fully Homomorphic Encryption on a Single GPU — 階層化と次元削減による大規模検索            |



### 3\. 周辺分野

* [Searchable encryption: A survey](https://doi.org/10.1080/19393555.2022.2033367?utm_source=chatgpt.com) — Sharma, 2023。専門家以外の読者も意識した総説。

* [A Survey on Searchable Symmetric Encryption](https://doi.org/10.1145/3617991?utm_source=chatgpt.com) — Feng et al., 2024。検索可能暗号の方式、索引構造、情報漏洩などを整理。


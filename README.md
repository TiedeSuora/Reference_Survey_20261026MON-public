# Reference_Survey_20261026MON-public
Reference_Survey_20261026MON-public

# 文献_20261125WED_123407.txt

# Topic 0388_XXXXXXX_KK_20261124TUE_181110.txt
# - 2026.11.24(Tue) 18:11:10
**2026-11-24(Tue) 18:11:10**
Tue Nov 24 09:11:10 UTC 2026
Tue Nov 24 04:11:10 EST 2026
Tue Nov 24 05:11:10 EDT 2026
Tue Nov 24 18:11:10 JST 2026



# - 2026.11.25(Wed) 12:34:07
**2026-11-25(Wed) 12:34:07**

「3.3 比較・ランキング・Top-k」を最優先にするのがよい。

しかも、今回の目的は、すべての論文を完全に理解することではなく、まず先行研究を整理。

それなら、かなり効率よく進められそうです。

以前から考えていた FHE Vector Search は、大まかに

\\boxed{
\\text{距離計算}
\\longrightarrow
\\text{順位付け}
\\longrightarrow
\\text{Top-k 抽出}
}

という構造でした。

このうち、CKKS で比較的素直に実装できるのは距離計算です。

難しいのは、暗号化された距離の大小比較と、そこから上位 件を取り出す処理です。

NOMOS も、まさにこの問題を扱っていましたね。

したがって、3.3 を優先するのは、技術的にも進捗報告の組み立てとしても自然です。

### 📚 おすすめの文献調査順序

3.3に記載された4項目と、NOMOS の参考文献を踏まえると、次の順番をおすすめ。

| 優先度 | 論文                        | 理由               |
| --- | ------------------------- | ---------------- |
| 済   | NOMOS（2026）               | 全体像を把握済み         |
| 1   | Mazzone et al.（2025）      | NOMOS の順位計算の基礎   |
| 2   | Rovida et al.（2025）       | CKKS の比較・ソートの効率化 |
| 3   | Azogagh et al.（2024/2025） | 比較を避ける別方式        |
| 4   | Engorgio（2025）            | 暗号化検索システムとの比較    |

特に Mazzone et al. は、NOMOS が直接参考にしている研究です。

しかも、無料で全文を入手できます。

[Efficient Ranking, Order Statistics, and Sorting under CKKS — USENIX Security 2025](https://www.usenix.org/conference/usenixsecurity25/presentation/mazzone?utm_source=chatgpt.com)

論文のほか、発表スライドも公開されています。USENIX +1

こちらも参考になります。

[Lightweight Sorting in Approximate Homomorphic Encryption — Rovida et al.](https://eprint.iacr.org/2025/1150?utm_source=chatgpt.com)[A Non-Comparison Oblivious Sort and Its Application to Private k-NN — Azogagh et al.](https://petsymposium.org/popets/2025/popets-2025-0093.php?utm_source=chatgpt.com)

ただし、Mazzone や Rovida はランキング・ソートそのものの研究なので、検索システム全体の性能評価とは分けて考える必要があります。

### 🍵 当面は、ここだけで十分

まず Mazzone の論文をダウンロードして、NOMOS と何が違うのかを整理するところまでを次の小さな目標にします

==========================================================================

# Metdho Name: KP-PRE
- Sovling image alignment failes occurs
- Motivation: Relative Position Encoding can only inject the model with prior knowledge that nearby pixels are more important than far pixels.
the significance of pixels is not solely dictated by their proximity but also by their relative positions to specific keypoints within the image

# Alignment
- ##### definition: transform images into a consistent and standardized from, often by scaling, rotating, and translating.
- ##### Problem of Alignment: This standardization helps recognition models learn the underlying patterns and features more effectively. As a result, many state-of-the-art (SoTA) face recognition models rely on well-aligned datasets to achieve high accuracy.
# KeyPoint
- definition: serve as representative points that capture the essential structure or layout of an object
# Absolute Position Encoding
- To address the problem that self-attention mechanism does not consider input token positions
$$
x_i' = x_i + \mathrm{PE}(i)
$$
- embeddings are generated using sinusoidal functions or learned directly.
# Relatvie Position Encoding
- definition: considers query-key interactions based on sequence-relative distances
- capture the relative spatial relationships among regions of an image, learning the positional dependencies without relying on absolute coordinates.
- ##### Limitaion: even if an image changes in terms of scaling, shifting, or orientation, the significance of the key-query position in RPE stays the same.
$$
e_{ij}' = \frac{(\mathbf{Q}_i + \mathbf{R}_{ij}^{Q})(\mathbf{K}_j + \mathbf{R}_{ij}^{K})^T}{\sqrt{d_k}}, \quad 
\mathbf{Y}_i = \sum_{j=1}^{n} a_{ij}(\mathbf{V}_j + \mathbf{R}_{ij}^{V}).
$$
### 🧩 各參數說明

| 參數                        | 說明                                                   |
| ------------------------- | ---------------------------------------------------- |
| $$\mathbf{Q}_i$$          | 第 \(i\) 個位置的 Query 向量（來自輸入特徵）                        |
| `\(\mathbf{K}_j\)$        | 第 \(j\) 個位置的 Key 向量                                  |
| `\(\mathbf{V}_j\)`        | 第 \(j\) 個位置的 Value 向量                                |
| `\(\mathbf{R}_{ij}^{Q}\)` | 第 \(i\) 個 query 對應第 \(j\) 個 key 的相對位置編碼（針對 query 向量） |
| `\(\mathbf{R}_{ij}^{K}\)` | 相對位置編碼，針對 key 向量的部分                                  |
| `\(\mathbf{R}_{ij}^{V}\)` | 相對位置編碼，針對 value 向量的部分                                |
| `\(d_k\)`                 | Query/Key 的維度，用於 softmax 前的標準化                       |
| `\(a_{ij}\)`              | softmax 計算後的注意力權重                                    |

# Keypoint Relative Position Encoding

##### Techinique:
- By adding relative position encodings into the queries and keys, the model can effectively learn positional dependencies without relying on absolute coordinates. 

# KP-PRE
- dynamically adapts(key, query) based on image keypoints(facial landmark)

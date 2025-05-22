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
- 
$$
# PRE
- capture the relative spatial relationships among regions of an image, learning the positional dependencies without relying on absolute coordinates.
- ##### Limitaion: even if an image changes in terms of scaling, shifting, or orientation, the significance of the key-query position in RPE stays the same.
##### Techinique:
- By adding relative position encodings into the queries and keys, the model can effectively learn positional dependencies without relying on absolute coordinates. 

# KP-PRE
- dynamically adapts(key, query) based on image keypoints(facial landmark)

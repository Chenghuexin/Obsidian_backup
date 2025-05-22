==========================================================================

# Metdho Name: KP-PRE
- Sovling image alignment failes occurs
- Motivation: Relative Position Encoding can only inject the model with prior knowledge that nearby pixels are more important than far pixels.
the significance of pixels is not solely dictated by their proximity but also by their relative positions to specific keypoints within the image

# Alignment
- ##### definition: transform images into a consistent and standardized from, often by scaling, rotating, and translating.
- ##### Problem of Alignment: This standardization helps recognition models learn the underlying patterns and features more effectively. As a result, many state-of-the-art (SoTA) face recognition models rely on well-aligned datasets to achieve high accuracy.

# PRE
- capture the relative spatial relationships among regions of an image, learning the positional dependencies without relying on absolute coordinates.
- ##### Limitaion: even if an image changes in terms of scaling, shifting, or orientation, the significance of the key-query position in RPE stays the same.
- ##### Te

# KP-PRE
- dynamically adapts(key, query) based on image keypoints(facial landmark)

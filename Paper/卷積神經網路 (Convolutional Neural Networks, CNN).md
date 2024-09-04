---
media: https://www.youtube.com/watch?v=OP5HcXJg2Aw
---
# Pattern

# Receptive field

# Typical Setting 

- kernel size (3x3)
- stride : 移動範圍(2)
- padding : receptive field有超出範圍的部分，使用padding補足

# Parameter sharing

each receptive field has the neurons with the same set of parameters(**Filter**)

# Pooling

主要目的為減少運算量，但近年來因為運算能力越來越進步，開始減少使用Pooling

# Flatten

將所有矩陣拉直變成一個向量，接著再把這個向量丟入全連階層
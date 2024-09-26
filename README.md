# Vison-Transformer-using-Pytorch
Scratch Implementation of Vison Transformer using python libraries-Pytorch
The repository contains a Jupiter notebook with scratch implementation of a Vision tyransformer from pytorch. The purpose of this reprository is to understand the key components of a vision Transformer.
Below is the basic architechture of a vision transformer.
![image](https://github.com/user-attachments/assets/838e5afd-df5a-4b8d-9a5c-9d53467a3003)
**Input representation**:
The images are divided into patches(generally, of size 16x16) and then flaatened to linearly project them to some latent dimension. </br>
We add positional encoding to the patches so that the model knows the sequence of the patches in the input image. Also, positional encoding helps in parallel attentio mechanism of the transformer.</br>
Positional Encoding can be done in two ways:
1.  The token can be made a learnable parameter which can be learned through attention layers.
2.  The following alternate sine and cosine method is the determistic way of performing positional encoding.
![image](https://github.com/user-attachments/assets/16673bc8-5907-49cf-8d9b-702cb1226cc7)
At last, an extra class token is appended to the image embedding which i =s learned throgh layers and is used for classification in the last layer. Due to attention layers, the class token contains semantic informatio of each patch of the input image an therefore is useful in image classification.



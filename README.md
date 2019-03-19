#  Pytorch implementation of Unet++ 

 Just use its main idea, the model is not the same as the origin unet++ mentioned in paper
paper : [UNet++: A Nested U-Net Architecture for Medical Image Segmentation](https://arxiv.org/abs/1807.10165)
## Architecture
　　　　　　　　　　　　　　y0　　　　y1　　　　 y2  
　　　　　　　　　　　　　　↑　　　　　↑　　　　　↑  
　　input　 → 　x1　 → 　　x11　→　　 x12 　→ 　 x  
　　　　　　　　　↘  　　↗    　　　　 ↗   　　　　 ↗  
　　　　　　　　　　　x2 　→　 　x21　 → 　x  
　　　　　　　　　　　　↘ 　　↗   　　　 ↗  
　　　　　　　　　　　　　　x3 　→　 x  
　　　　　　　　　　　　　　　↘　↗  
　　　　　　　　　　　　　　　　x4  
Notice: For ease of drawing , I have omitted some of the connections ,including x2 to x , x1 to x12 , x1 to x , x11 to x
              
    

## Wednesday (7/28) Response

(1) Show Images and Results

Primary Image:
![img_86.png](img_86.png)

Art Image:
![img_85.png](img_85.png)

![img_88.png](img_88.png)

Final Product:
![img_87.png](img_87.png)

(2) What do these images mean to you?

- 	The two images I choose convey my jump start experience, as well as my summer as a whole, very well. 
     The first image is a picture of a random dog wearing glasses while reading a book. This image carries several 
     different meanings. The first is that this summer I have had a lot of work I’ve had to manage due to the heavy 
     workload of the program. The second is that the image is of a dog, which reminds me of my dog, who  I credit 
     with keeping much of my stress down this summer. The second image I used was of the famous painting A Sunday 
     Afternoon on the Island of La Grande Jatte. I choose this image because I actually got to see it in person in late 
     June of this year when I visited Chicago to see my girlfriend. This relates to the class because even with the 
     heavy workload of the jump-start program, I still got to have a fun summer and partake in lots of cool and new 
     things.

(3) Steps

- (1) Define content and style representations

     - The first step of the model is to get the content and style versions of the image. To do this a VGG19 network is 
     used, which is a pretrained classification network that works specifically on images. The layers of the network
       work to define the images.
       
- (2) Extracting style and content

     - This second step is fairly simple, this where the model is built. The model that is created here should output
     the style and content images as tensors.
       
- (3)Implementing the style transfer algorithm

     - The style transfer algorithm works by calculating mean square error of the image's output in coordination with
     the targets. After this, the weighted sum of each is taken on the losses.

- (4) Apply regularization term on the high frequency components

     - The fourth and final step is to do some regularization. The basic implementation used up to this point 
       unfortunately leads to an abundance of high frequency artifacts. This step looks to address this issue. 
       To go about decreasing them an explicit regularization term is used on the components with a very high
       frequency. This step is often time referred to as total variance lost.

(4) What my work means in relation to my future in data science

- Along with the points I mentioned earlier, these images also can be related to my future in data science. The first
image represents me having to work really hard to get to where I want to be in my career. A career in data science will
  take a lot of work and effort and I feel the first image represents that well. The second image doesn't connect too
  well but if I had to make a connection I would say that since the painting is in Chicago, and Chicago has lots of tall 
  buildings, it represents my knowledge in data science going up.


(5) Stretch Goal (Deep Dream)


![img_89.png](img_89.png)

![img_90.png](img_90.png)

![img_91.png](img_91.png)

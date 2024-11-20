# Project5 **The Power of Diffusion Models**

## **Part A of a Larger Project**

### **Overview**

In Part A of this project, we explore the capabilities of diffusion models. We implement diffusion sampling loops and apply them to tasks such as inpainting and creating optical illusions. 

### **Part 1: Sampling Loops**

#### **1.1 Implementing the Forward Process**

**Test Image at Noise Levels [250, 500, 750]**

![1](./images/1.jpg)

#### **1.2 Classical Denoising**

For each noisy image, we applied Gaussian blur to attempt denoising.

![2](./images/2.png)

#### **1.3 One-Step Denoising**

Using the UNet model to estimate and remove noise.

<img src="./images/30.png" alt="30" style="zoom:400%;" />

<img src="./images/31.png" alt="31" style="zoom:67%;" />

<img src="./images/32.png" alt="32" style="zoom:67%;" />

<img src="./images/33.png" alt="33" style="zoom:67%;" />

#### **1.4 Iterative Denoising**

**Denoising Process (Every 5th Image)**

![download](./images/download.png)

<img src="./images/download-2.png" alt="download-2" style="zoom:72%;" />

<img src="./images/download-3.png" alt="download-3" style="zoom:72%;" />

<img src="./images/download-4.png" alt="download-4" style="zoom:72%;" />

<img src="./images/download-5.png" alt="download-5" style="zoom:72%;" />



**Comparison with One-Step Denoising and Gaussian Blurring**

​	•	*One-Step Denoised Image*

<img src="./images/download-6.png" alt="download-6" style="zoom:72%;" />

​	•	*Gaussian Blurred Image*

<img src="./images/gau.png" alt="gau" style="zoom:72%;" />

#### **1.5 Diffusion Model Sampling**

We generated images from random noise using the iterative denoising process.

**Sampled Images**

<img src="./images/5.png" alt="5" style="zoom:25%;" />

<img src="./images/download-7.png" alt="download-7" style="zoom:25%;" />

<img src="./images/download-8.png" alt="download-8" style="zoom:25%;" />

<img src="./images/download-9.png" alt="download-9" style="zoom:25%;" />

<img src="./images/download-10.png" alt="download-10" style="zoom:25%;" />

#### **1.6 Classifier-Free Guidance (CFG)**

**Generated Images with CFG Scale = 7**

<img src="./images/download-11.png" alt="download-11" style="zoom:25%;" />

<img src="./images/download-12.png" alt="download-12" style="zoom:25%;" />

<img src="./images/download-13.png" alt="download-13" style="zoom: 67%;" />

<img src="./images/download-14.png" alt="download-14" style="zoom: 67%;" />

<img src="./images/download-16.png" alt="download-16" style="zoom:67%;" />

#### **1.7 Image-to-image Translation**

We applied the iterative denoising process to noisy versions of images.

**Edits of Test Image at Noise Levels [1, 3, 5, 7, 10, 20]**

![WeChat3b5105ca04bacff2241811e5869c884d](./images/WeChat3b5105ca04bacff2241811e5869c884d.jpg)

**Edits of Own Test Images**

![7](./images/7.jpg)

![WeChat20cfd01c60138606de0c9f4041df5eab](./images/WeChat20cfd01c60138606de0c9f4041df5eab.jpg)

##### **1.7.1 Editing Hand-Drawn and Web Images**

![WechatIMG296](./images/WechatIMG296.jpg)

![7.1](./images/7.1.jpg)

![WechatIMG298](./images/WechatIMG298.jpg)

##### **1.7.2 Inpainting**



**Inpainted Test Image**

<img src="./images/download-15.png" alt="download-15" style="zoom:72%;" />

<img src="./images/WechatIMG301.jpg" alt="WechatIMG301" style="zoom:72%;" />

**Own Images Edited**

*Image 1*

​	•	*Original*

<img src="./images/download-19.png" alt="download-19" style="zoom:200%;" />

​	•	*Mask*

<img src="./images/download-18.png" alt="download-18" style="zoom: 50%;" />

​	•	*Inpainted*

<img src="./images/download-33.png" alt="download-33" style="zoom:130%;" />

​		If we reverse the mask:

<img src="./images/download-20.png" alt="download-20" style="zoom: 50%;" />

*Image 2*

​	•	*Original*

<img src="./images/download-22.png" alt="download-22" style="zoom:200%;" />

​	•	*Mask*

<img src="./images/download-21.png" alt="download-21" style="zoom: 50%;" />

​	•	*Inpainted*

![download-38](./images/download-38.png)

![download-32](./images/download-32.png)

##### **1.7.3 Text-Conditional Image-to-image Translation**

**Edits of Test Image with Given Prompt**

![WeChatb0985639ad48a31115fd4aab0e2cbe77](./images/WeChatb0985639ad48a31115fd4aab0e2cbe77.jpg)

**Edits of Own Test Images**

​	•	*Image 1*

![WeChat952ea3d8c3139ca8bec1227993b6ab7d](./images/WeChat952ea3d8c3139ca8bec1227993b6ab7d.jpg)

​	•	*Image 2*

![WeChatbb72a682a0753ab5fef36c77058755c1](./images/WeChatbb72a682a0753ab5fef36c77058755c1.jpg)



#### **1.8 Visual Anagrams**





**Visual Anagram: “Old Man” and “People Around a Campfire”**

![download-34](./images/download-34.png)

![8](./images/8.png)





![download-35](./images/download-35.png)

![download-27](./images/download-27.png)





**Additional Illusions**

​	•	*Illusion 1*: ["a lithograph of waterfalls"], ["a photo of a man"]

​	•	*Image*

![download-37](./images/download-37.png)

​	•	*Flipped*

![download-29](./images/download-29.png)

​	•	*Illusion 2*: ["a photo of the amalfi cost"], ["a photo of a dog"]

​	•	*Image*

![download-36](./images/download-36.png)

​	•	*Flipped*

![download-28](./images/download-28.png)

#### **1.9 Hybrid Images**





**Hybrid Image: “Skull” and “Waterfall”**

​	•	*Resulting Image*

![WechatIMG305](./images/WechatIMG305.jpg)

![WechatIMG307](./images/WechatIMG307.jpg)

**Additional Hybrid Images**

​	•	*Hybrid Image 1*': a lithograph of a forest scene', 'a lithograph of hulk's face'

![WechatIMG310](./images/WechatIMG310.jpg)

![WechatIMG309 1](./images/WechatIMG309 1.jpg)

​	•	*Hybrid Image 2*: 'a lithograph of a skull', 'an oil painting of a snowy mountain village'

![WechatIMG312](./images/WechatIMG312.jpg)

![WechatIMG311](./images/WechatIMG311.jpg)

#### **Conclusion**

In this project, we explored the capabilities of diffusion models through various implementations and applications. We observed how iterative denoising improves image quality over single-step methods, and how techniques like CFG enhance the results further. By experimenting with image translation, inpainting, visual anagrams, and hybrid images, we demonstrated the versatility and power of diffusion models in generating and manipulating images.


<h1 align="center">Image-Based-Steganography-using-Python</h1>
<img src="https://www.jigsawacademy.com/wp-content/uploads/2021/01/CS-01-1-2-1024x352.jpg" alt="Image Hiding" align="center"/>
 <br>
 <h4 align = "center">Python based Image steganography project which uses LSB (Least Significant Bit) algorithm for encoding .
  <br>
 
 ### `What is Steganography?`
 
 <p>Steganography is the process of hiding a secret message within another file  in such a way that someone can not know the presence or contents of the hidden message.
 </p>

 ### `Types of Steganography`
 <p>
  Steganography works have been carried out on different transmission media like images, video,     text, or audio.
 </p>
 
 <img src= "https://www.researchgate.net/profile/Jamil-Ahmad-13/publication/267269624/figure/fig1/AS:295642766299140@1447498136848/Types-of-Steganography-wrt-carrier-object.png"  alt="Types of Steganography" align="center"/>
 
 ### `Basic Steganographic Model`
 <img src="https://miro.medium.com/max/875/0*fwfkaK09mCKlWrJc" alt="Model" align="center" />
 <p>As seen in the above image, both the original image file(X) and secret message (M) that needs to be hidden are fed into a steganographic encoder as input. Steganographic Encoder function, f(X,M,K) embeds the secret message into a cover image file by using techniques like least significant bit encoding. The resulting stego image looks very similar to your cover image file, with no visible changes. This completes encoding. To retrieve the secret message, stego object is fed into Steganographic Decoder. </p>
 
 ### `Least Significant Bit Steganography`
 
  <p>The idea behind image-based Steganography is very simple. Images are composed of digital data (pixels), which describes what’s inside the picture, usually the colors of all the pixels. Since we know every image is made up of pixels and every pixel contains 3-values (red, green, blue).
 

Encode the data :
Every byte of data is converted to its 8-bit binary code using ASCII values. Now pixels are read from left to right in a group of 3 containing a total of 9 values. The first 8-values are used to store binary data. The value is made odd if 1 occurs and even if 0 occurs.
 
 
Decode the data :
To decode, three pixels are read at a time, till the last value is odd, which means the message is over. Every 3-pixels contain a binary data, which can be extracted by the same encoding logic. If the value if odd the binary bit is 1 else 0.</p>
 

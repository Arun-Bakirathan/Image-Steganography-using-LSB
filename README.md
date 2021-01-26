# Image-Steganography-using-LSB
Image Steganography using LSB algorithm

**Introduction**
Steganography
Literally means “covered writing” in (Greek) .
Hiding messages in innocent media.
Steganography may or may not be used in conjunction with cryptography.
So, you may possibly encrypt the message before hiding

**Terminology**
 Multimedia files are typically used to hide messages like
images, sound files, movies, binary files, text files
 Like you see, you
have seen the IP packets, network packets, there are some fields which are unused. Those
unused bits can also be used to carry some message or information. 

**Steganography in image files**
 size of my image determined by ‘pixels’. A pixel is instance of color.
        1. fundamental colors RGB, as combination of Red, Green and Blue.
         2. Each color in 8 bits the value can between 0 and 255 
         3. eg:00 00 00 is black ,FF 00 00 is red, FF FF FF is white.
Each pixel is  represented by an 8-bit value(gif) or24 bit value(JPEG or BMP)

The image data is usally compressed by
              * Lossless compression – that exact pixel value stored
              * Lossy compression – approximate pixel values are stored 

**Meathods**
Least significant bit(LSB):  modify the LSB of pixel value based on the message to hide. small changes in pixel value cant noticed by human observers.
Properties:
                           > simple to implement 
                           > compatible with lossless compression
                           > better adapted with 24 bit images
                           > extremely vulnerable to image manipulation
                           
                           
                          

**Algorithm**
Suppose we want to hide the letter ‘c’ in a gif image. The ASCII value of ‘c’ is 67 , ie 01000011.
Suppose that the first eight pixels of gif image are:
      00110101    01001000    00101000     00110101
      00101111    00011100    01001000     01001000
Modifying the LSB corresponding to ‘c’ gives
       00110100    01001001      00101000    00110100
       00101110    00011100      01001001    01001001
 changes in the index values (in the color-map table ) may lead to easily detectable pattern in the image

**sample outputs**

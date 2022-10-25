Title of mini project :- Hybrid Approach to Text & Image Steganography using AES and LSB Technique 

Platform we are using :-
Python : Python is an interpreted, object-oriented, high-level programming language with dynamic semantics. Its high-level built in data structures, combined with dynamic typing and dynamic binding, make it very attractive for Rapid Application Development, as well as for use as a scripting or glue language to connect existing components together. Python's simple, easy to learn syntax emphasizes readability and therefore reduces the cost of program maintenance.

Softwares we are using 
Pycharm : An IDE can help you code faster and become much more productive if you devote some time to learning the tool in the first place. As an IDE for Python and other languages, PyCharm gives you highly accurate code completion that helps you write less code and avoid bugs. With its smart code navigation, you can quickly navigate around your code to inspect, for instance, the implementation of a class you are about to instantiate. PyCharm’s project-wide refactorings will ensure you won’t break any code when, for instance, renaming a variable or changing a method signature, and much more.

Problem statement: -
In the existing system the image or text is directly hidden in the cover image. Thus hacker/intruder can use Steg-Analyser and extract the least significant bits and then convert it back to original form. The system supports only a few image types, thus only a limited number of users are benefitted. Cover images may be more polluted or noise is more when storing large data. 
In our project the system first encrypts the given message using AES encryption and then it is written on to the cover image. This provides very high security. The system supports 24-bit and 32-bit BMP images. The system uses a unique LSB technique which stores more data than the original algorithm and also maintains good quality while doing so.










Proposed method:
Algorithm 

       AES (mode - EAX) 
           Encrypt-then-authenticate-then-translate is a mode of operation performed on cryptographic block ciphers. 
           It is a flexible nonce-using two pass AEAD (Authenticated Encryption with Associated Data) 

       LSB 
        Firstly, we input the data that is to be encrypted into the cover image, this could be either text data or image data. 
        Then input the cover image into which the used inteds to embed the actual data.
        Input the RGB  pixel values of the cover image. 
        In case of an image data, for each component of the pixel, we replace the two rightmost bits in either R/G/B if it’s in the highest among them 
        and is above a threshold value. 
        Repeat the previous two steps till the completion of the text or the image. 
        Produce the output of the generated Stego image. 


Firstly, we input the data that is to be encrypted into the cover image, this could be either text data or image data. 
Then input the cover image into which the used inteds to embed the actual data.
Input the RGB  pixel values of the cover image. 
In case of an image data, for each component of the pixel, we replace the two rightmost bits in either R/G/B if it’s in the highest among them and is above a threshold value. 
Repeat the previous two steps till the completion of the text or the image. 
Produce the output of the generated Stego image. 

Modules used in project:-
CV2
Numpy
PIL
Cryptodome

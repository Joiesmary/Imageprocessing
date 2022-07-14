    # Imageprocessing
    program1: 

         import cv2
         img=cv2.imread('rose3.jpg',0)
         cv2.imshow('image',img)
         cv2.waitKey(0)
         cv2.destroyAllWindows()
   
   
![image](https://user-images.githubusercontent.com/19484531/178718441-4440fea5-3bf4-42a8-8387-86c5b974dac3.png)


program2 :

        import matplotlib.image as mping
         import matplotlib.pyplot as plt
        img=mping.imread('rose3.jpg')
        plt.imshow(img)
        
        
![image](https://user-images.githubusercontent.com/19484531/178719601-982d4b07-1546-4639-a20e-379ecc821323.png)

     program3: 
          import cv2
          from PIL import Image
          img=Image.open("rose3.jpg")
          img=img.rotate(180)
          img.show()
          cv2.waitKey()
          cv2.destroyAllWindows()


![image](https://user-images.githubusercontent.com/19484531/178720354-dd3048b0-3857-4ab0-967f-989d407bb1a3.png)

    program4: 

     from PIL import ImageColor
     img1=ImageColor.getrgb("yellow")
      print(img1)
      img2=ImageColor.getrgb("red")
      print(img2)
      img2=ImageColor.getrgb("blue")
      print(img2)
      
         output:
         (255, 255, 0)
         (255, 0, 0)
          (0, 0, 255)
          
          
          program5:
          from PIL import Image
          img=Image.new('RGB',(200,400),(255,255,0))
         img.show()
         img=Image.new('RGB',(200,400),(0,0,255))
          img.show()
          
          
 ![image](https://user-images.githubusercontent.com/19484531/178720896-1f88e981-d828-48cb-b2fe-bbcf7dede17f.png)
      
![image](https://user-images.githubusercontent.com/19484531/178720950-32826468-7c8c-4615-90ea-1a903e2436b0.png)


      program6: 

      import cv2
      import matplotlib.pyplot as plt
      import numpy as np
      img=cv2.imread('butterfly.jpg')
      plt.imshow(img)
      plt.show()
      img=cv2.cvtColor(img,cv2.COLOR_RGB2BGR)
      plt.imshow(img)
      plt.show()
      img=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
      plt.imshow(img)
      plt.show()
   
 ![image](https://user-images.githubusercontent.com/19484531/178945094-2a315d26-032e-463d-b797-44cafc413585.png)

    program 7:
    
      from PIL import Image
     image=Image.open('rose3.jpg')
      print("File Name:",image.filename)
      print("Fromat:",image.format)
      print("Mode:",image.mode)
      print("size:",image.size)
      print("Width:",image.width)
      print("Height:",image.height)
      image.close()
      
      Out put: 
      File Name: rose3.jpg
      Fromat: JPEG
      Mode: RGB
      size: (205, 245)
      Width: 205
      
      program 8:
      import cv2
      img=cv2.imread('dog3.jpg')
      cv2.imshow("RGB",img)
      cv2.waitKey(0)
      img=cv2.imread('dog3.jpg',0)
      cv2.imshow("Gray",img)
      cv2.waitKey(0)
      ret,bw_img=cv2.threshold(img,127,255,cv2.THRESH_BINARY)
      cv2.imshow("Binary",bw_img)
      cv2.waitKey(0)
      cv2.destroyAllWindows()
      
 ![image](https://user-images.githubusercontent.com/19484531/178965223-01d750cd-d0ea-404b-bb4a-dae8b83b08e2.png)
 ![image](https://user-images.githubusercontent.com/19484531/178965346-58b2749f-2b98-47f8-a105-916418e35898.png)
![image](https://user-images.githubusercontent.com/19484531/178965411-082a14d2-c50d-494d-86b0-ddcc1c69209a.png)


     program 9:
     import cv2
     img=cv2.imread('plant2.jpg')
     print('original image length width',img.shape)
     cv2.imshow('Original image',img)
     cv2.waitKey(0)
     imgresize=cv2.resize(img,(150,160))
     cv2.imshow('Resize image',imgresize)
     print('Resized image length width',imgresize.shape)
     cv2.waitKey(0)
     
     output:
     original image length width (195, 259, 3)
     
     program 10:
     from skimage import io
      import matplotlib.pyplot as plt
      url='https://images.unsplash.com/photo-1573692822343-a4c703f8043c?ixlib=rb-     1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8bW9uYXJjaCUyMGJ1dHRlcmZseXxlbnwwfHwwfHw%3D&w=1000&q=80'
     image=io.imread(url)
     plt.imshow(image)
     plt.show()
     
 ![image](https://user-images.githubusercontent.com/19484531/178965792-bec6d5ef-f372-4046-b96a-e60b65b60a24.png)



Height: 245

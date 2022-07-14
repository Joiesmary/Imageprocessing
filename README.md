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

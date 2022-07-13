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


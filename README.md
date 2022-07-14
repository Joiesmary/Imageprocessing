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



     program 11: 
    import cv2
    import matplotlib.image as mping
    import matplotlib.pyplot as plt
    img=mping.imread('rose1.jpg')
    plt.imshow(img)
    plt.show()
    
    
![image](https://user-images.githubusercontent.com/19484531/178966069-f68729e8-2d58-4a66-910d-ea5e54b97508.png)

    hsv_img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
    light_orange=(1,190,200)
    dark_orange=(18,255,255)
    mask=cv2.inRange(hsv_img,light_orange,dark_orange)
    result=cv2.bitwise_and(img,img,mask=mask)
    plt.subplot(1,2,1)
    plt.imshow(mask,cmap="gray")
    plt.subplot(1,2,2)
    plt.imshow(result)
    plt.show()
![image](https://user-images.githubusercontent.com/19484531/178966232-4503e02c-d3e7-46ca-9057-b7e2ff02e7f7.png)

    light_white=(0,0,200)
    dark_white=(142,60,255)
    mask_white=cv2.inRange(hsv_img,light_white,dark_white)
    result_white=cv2.bitwise_and(img,img,mask=mask_white)
    plt.subplot(1,2,1)
    plt.imshow(mask_white,cmap="gray")
    plt.subplot(1,2,2)
    plt.imshow(result_white)
    plt.show()
  
![image](https://user-images.githubusercontent.com/19484531/178966395-c5663b82-dfa1-4eff-adf9-0343f9a4748b.png)
  
    final_mask=mask+mask_white
    final_result=cv2.bitwise_and(img,img,mask+final_mask)
    plt.subplot(1,2,1)
    plt.imshow(final_mask,cmap="gray")
    plt.subplot(1,2,2)
    plt.imshow(final_result)
    plt.show()
    
![image](https://user-images.githubusercontent.com/19484531/178966541-7874a799-2f84-43d8-9493-a4545284094a.png)

    blur=cv2.GaussianBlur(final_result,(7,7),0)
    plt.imshow(blur)
    plt.show()
    
![image](https://user-images.githubusercontent.com/19484531/178966622-77940c15-413c-4b9c-87e2-a9adc4524f9d.png)


program 12:

      import cv2
      import matplotlib.image as mping
      import matplotlib.pyplot as plt
      img1=cv2.imread('butterfly.jpg')
      img2=cv2.imread('butterfly.jpg')
      fimg1=img1+img2
      plt.imshow(fimg1)
      plt.show()
      cv2.imwrite('output.jpg',fimg1)
      fimg2=img1-img2
      plt.imshow(fimg2)
      plt.show()
      cv2.imwrite('output.jpg',fimg2)
     fimg3=img1*img2
     plt.imshow(fimg3)
     plt.show()
     cv2.imwrite('output.jpg',fimg3)
    fimg4=img1/img2
    plt.imshow(fimg4)
    plt.show()
    cv2.imwrite('output.jpg',fimg4)
 ![image](https://user-images.githubusercontent.com/19484531/178966985-180e1518-620b-409a-b2f3-ba3f18bafce4.png)
 
 ![image](https://user-images.githubusercontent.com/19484531/178967089-63d5f0a0-1fdb-4a39-bc7b-4fbb71ede823.png)


    program 13:
    
    import cv2
    img=cv2.imread("D:\i.jpg")
    gray=cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
    hsv=cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
    lab=cv2.cvtColor(img,cv2.COLOR_BGR2LAB)
    hls=cv2.cvtColor(img,cv2.COLOR_BGR2HLS)
    yuv=cv2.cvtColor(img,cv2.COLOR_BGR2YUV)
    cv2.imshow("Gray image",gray)
    cv2.imshow("Hsv image",hsv)
    cv2.imshow("Lab image",lab)
    cv2.imshow("Hls image",hls)
    cv2.imshow("Yuv image",yuv)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
    
 ![image](https://user-images.githubusercontent.com/19484531/178967627-481e7c6b-6a47-4055-aaee-94581610abdb.png)


     program 14: 
     
     import cv2 as c
     import numpy as np
     from PIL import Image
     array=np.zeros([100,200,3],dtype=np.uint8)
     array[:,:100]=[255,130,0]
     array[:,100:]=[0,0,255]
    img=Image.fromarray(array)
    img.save('image1.png')
    img.show()
    c.waitKey(0)

![image](https://user-images.githubusercontent.com/19484531/178967844-db289dd0-5827-4f83-8752-196e27b40f75.png)


      program 15:
   
      import cv2
      import matplotlib.image as mping
       import matplotlib.pyplot as plt
      image1=mping.imread('bird1.jpg')
      image2=mping.imread('bird1.jpg')
      ax=plt.subplots(figsize=(15,10))
      bitwiseAnd= cv2.bitwise_and(image1, image2) 
      bitwiseor= cv2.bitwise_or(image1, image2)
      bitwiseXor=cv2.bitwise_xor (image1,image2) 
      bitwiseNot_img1= cv2.bitwise_not(image1)
      #bitwiseNot_img1= cv2.bitwise_not(image2)
      plt.subplot(151)
      plt.imshow(bitwiseAnd)
      plt.subplot(152)
      plt.imshow(bitwiseor)
      plt.subplot(153)
      plt.imshow(bitwiseXor)
      plt.subplot(154)
      plt.imshow(bitwiseNot_img1) 
     #plt.subplot(155)
     #plt.imshow(bitwiseNot_img2)
      cv2.waitKey(0)
   

![image](https://user-images.githubusercontent.com/19484531/178968074-2f45fc80-38ca-4cac-b888-458a1e7a677a.png)

  
      program 16: 
    
       import cv2
       import numpy as np
       image=cv2.imread('rose7.jpg')
       cv2.imshow('original Image',image)
       cv2.waitKey(0)
       Gaussian=cv2.GaussianBlur(image,(7,7),0)
       cv2.imshow('gaussian Bluring',Gaussian)
       cv2.waitKey(0)
       median=cv2.medianBlur(image,5)
       cv2.imshow('Median Bluring',median)
       cv2.waitKey(0)
       bilateral=cv2.bilateralFilter(image,9,75,75)
       cv2.imshow('Bilateral Bluring',bilateral)
       cv2.waitKey(0)
       cv2.distroyAllWindows()

![image](https://user-images.githubusercontent.com/19484531/178968398-250ea35f-e271-4617-8f97-745fac306ec2.png)
![image](https://user-images.githubusercontent.com/19484531/178968450-56d7abb5-48c9-4ed8-bf5d-8931373df326.png)
![image](https://user-images.githubusercontent.com/19484531/178968525-6e297678-73af-49bd-b03c-d6a19041d9cd.png)
![image](https://user-images.githubusercontent.com/19484531/178968575-aad10e47-cb05-4344-b005-0885365b1368.png)

      
          program 17:
          
          from PIL import Image
          from PIL import ImageEnhance
          image=Image.open('plant2.jpg')
          image.show()
          enh_bri=ImageEnhance.Brightness(image)
          brightness=1.5
          image_brightened=enh_bri.enhance(brightness)
          image_brightened.show()
         enh_col=ImageEnhance.Color(image)
         color=1.5
         image_colored=enh_col.enhance(color)
          image_colored.show()
         enh_con=ImageEnhance.Contrast(image)
         contrast=1.5
         image_contrasted=enh_con.enhance(contrast)
         image_contrasted.show()
          enh_sha=ImageEnhance.Sharpness(image)
          sharpness=3.0
          image_sharpness=enh_sha.enhance(sharpness)
           image_sharpness.show()
           
           
 ![image](https://user-images.githubusercontent.com/19484531/178968989-0ebff431-a2c1-4557-b1b1-8b3c807a0309.png)
 
 
       program 18:
       
       import cv2
       import numpy as np
       from matplotlib import pyplot as plt
       from PIL import Image,ImageEnhance
       img=cv2.imread('butterfly.jpg',0)
       ax=plt.subplots(figsize=(20,10))
       kernel=np.ones((5,5),np.uint8)
       opening=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
       closing=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
       erosion=cv2.erode(img,kernel,iterations=1)
       dilation=cv2.dilate(img,kernel,iterations=1)
       gradient=cv2.morphologyEx(img,cv2.MORPH_GRADIENT,kernel)
        plt.subplot(151)
        plt.imshow(opening)
         plt.subplot(152)
        plt.imshow(closing)
        plt.subplot(153)
        plt.imshow(erosion)
        plt.subplot(154)
      plt.imshow(dilation)
      plt.subplot(155)
       plt.imshow(gradient)
       cv2.waitKey(0)
       

 ![image](https://user-images.githubusercontent.com/19484531/178969280-d2b42e03-62f5-4c57-abde-b66bff4dc179.png)



       program 19:
       import cv2
       OriginalImg=cv2.imread('butterfly.jpg')
       GrayImg=cv2.imread('butterfly.jpg',0)
       isSaved=cv2.imwrite('D:/i.jpg',GrayImg)
       cv2.imshow('Display original image',OriginalImg)
       cv2.imshow('Display gray scal image',GrayImg)
       cv2.waitKey(0)
       cv2.destroyAllWindows()
       if isSaved:
            print('The image is successfully Saved')
            
            Out put:
          The image is successfully Saved
          
          
  ![image](https://user-images.githubusercontent.com/19484531/178969714-52b80b8d-e945-4bea-9207-44f5af297203.png)

![image](https://user-images.githubusercontent.com/19484531/178969827-e5a62560-b466-45af-bf3e-9533173b65c0.png)

    
       program 20:
    
       import cv2
       import numpy as np
       from matplotlib import pyplot as plt
       image=cv2.imread('dog3.jpg',0)
       x,y=image.shape
       z=np.zeros((x,y))
       for i in range(0,x):
          for j in range(0,y):
              if(image[i][j]>50 and image[i][j]<150):
                 z[i][j]=255
              else:
                 z[i][j]=image[i][j]
        equ=np.hstack((image,z))
        plt.title('Graylevel slicing with backgroug')
        plt.imshow(equ,'gray')
        plt.show()


![image](https://user-images.githubusercontent.com/19484531/178970074-b6b27003-3715-4a22-886c-f3a2efe1e0dc.png)

     
      program 21:
      
      import cv2
      import numpy as np
      from matplotlib import pyplot as plt
      image=cv2.imread('dog3.jpg',0)
      x,y=image.shape
      z=np.zeros((x,y))
      for i in range(0,x):
          for j in range(0,y):
               if(image[i][j]>50 and image[i][j]<150):
                   z[i][j]=255
               else:
                   z[i][j]=0
      equ=np.hstack((image,z))
      plt.title('Graylevel slicing with out background')
      plt.imshow(equ,'gray')
       plt.show()
       
  ![image](https://user-images.githubusercontent.com/19484531/178970255-09b2f243-52af-4214-be85-af997eccc554.png)
  
  
  
  
       program 22:
       
         import numpy as np
         import cv2 as cv
         from matplotlib import pyplot as plt
         img = cv.imread('rose3.jpg')
         plt.imshow(img)
         plt.show()
         img = cv.imread('rose3.jpg',0)
         plt.hist(img.ravel(),256,[0,256]);
         plt.show()
         
  

![image](https://user-images.githubusercontent.com/19484531/178970649-0e2c0045-44f6-4096-802c-610956b2c45e.png)

          from skimage import io
          import matplotlib.pyplot as plt
          img = cv.imread('rose3.jpg')
           plt.imshow(img)
          plt.show()
         ax = plt.hist(img.ravel(), bins = 256)
         _ = plt.xlabel('Intensity Value')
         _ = plt.ylabel('Count') 
         plt.show()
         
  ![image](https://user-images.githubusercontent.com/19484531/178970783-0026ddf8-a448-4ec8-8cb1-3533c511521f.png)
  
           from skimage import io
           import matplotlib.pyplot as plt
           img = io.imread('rose3.jpg')
           plt.imshow(img)
           plt.show()
           image = io.imread('rose3.jpg')
           ax = plt.hist(image.ravel(), bins = 256)
           plt.show()
           
 ![image](https://user-images.githubusercontent.com/19484531/178970904-254c7206-860a-4a06-ac34-7c298db2056d.png)





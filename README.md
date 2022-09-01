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
      img1=cv2.imread('butterfly.jpg') #img1=cv2.imread('catresize.jpg')
      img2=cv2.imread('butterfly.jpg')#img2=cv2.imread('dog3.jpg')
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
    
    output 1:
 ![image](https://user-images.githubusercontent.com/19484531/178966985-180e1518-620b-409a-b2f3-ba3f18bafce4.png)
 
 ![image](https://user-images.githubusercontent.com/19484531/178967089-63d5f0a0-1fdb-4a39-bc7b-4fbb71ede823.png)
     
     output 2:
![image](https://user-images.githubusercontent.com/19484531/183876467-a0118bd0-76db-42d2-88db-b2112d48a62f.png)
![image](https://user-images.githubusercontent.com/19484531/183876539-70481877-32fd-4303-b0bf-01bbea1b12e8.png)


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
        image1=mping.imread('catresize.jpg')
        image2=mping.imread('dog3.jpg')
        ax=plt.subplots(figsize=(15,10))
        bitwiseAnd=cv2.bitwise_and(image1,image2)
        bitwiseOr=cv2.bitwise_or(image1,image2)
        bitwiseXor=cv2.bitwise_xor(image1,image2)
        bitwiseNot_img1= cv2.bitwise_not(image1)
        bitwiseNot_img2= cv2.bitwise_not(image2)
        plt.subplot(151)
        plt.imshow(bitwiseAnd)
        plt.subplot(152)
        plt.imshow(bitwiseOr)
        plt.subplot(153)
        plt.imshow(bitwiseXor)
        plt.subplot(154)
        plt.imshow(bitwiseNot_img1)
        plt.subplot(155)
        plt.imshow(bitwiseNot_img2)
        cv2.waitKey(0)
   

![image](https://user-images.githubusercontent.com/19484531/183875236-acd0a5b3-2f2f-4c4e-9bf9-095740d09a8e.png)

  
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





      program 23:Image Processing Lab Exercise :20/07/2022
             1. Program to perform basic image data analysis using intensity transformation:
                  a) Image negative
                  b) Log transformation
                  c) Gamma correction
                  d)
 

        %matplotlib inline
        import imageio
        import matplotlib.pyplot as plt
        import warnings
        import matplotlib.cbook
        warnings.filterwarnings("ignore",category=matplotlib.cbook.mplDeprecation)
        pic=imageio.imread("butterfly.jpg")
        plt.figure(figsize=(6,6))
        plt.imshow(pic);
        plt.axis('off');
        
![image](https://user-images.githubusercontent.com/19484531/179949580-6ebaa4cf-5244-414e-8006-9683069e1037.png)


         negative=255-pic
         plt.figure(figsize=(6,6))
         plt.imshow(negative);
         plt.axis('off');
         
![image](https://user-images.githubusercontent.com/19484531/179949771-6a577bfe-a1b9-4d36-91ff-1028f3892e2b.png)


         %matplotlib inline
         import imageio
         import numpy as np
         import matplotlib.pyplot as plt
         pic=imageio.imread('butterfly.jpg')
         gray=lambda rgb:np.dot(rgb[...,:3],[0.299,0.587,0.114])
         gray=gray(pic)
         max_=np.max(gray)
         def log_transform():
               return(255/np.log(1+max_))*np.log(1+gray)
         plt.figure(figsize=(5,5))
         plt.imshow(log_transform(),cmap=plt.get_cmap(name='gray'))
         plt.axis('off');
         
         
![image](https://user-images.githubusercontent.com/19484531/179949989-0f1fcf30-ffa0-424e-9d44-4ea231698782.png)


         import imageio
         import matplotlib.pyplot as plt
         pic=imageio.imread('butterfly.jpg')
         gamma=2.2
         gamma_correction=((pic/255)**(1/gamma))
         plt.figure(figsize=(5,5))
         plt.imshow(gamma_correction)
         plt.axis('off');
         
![image](https://user-images.githubusercontent.com/19484531/179950134-1c5edc9a-d057-4e11-9c9d-77df34fc4907.png)


        if we give  ,
              gamma=5.5
              
![image](https://user-images.githubusercontent.com/19484531/179950350-67a80abc-4d96-45bb-90da-3e6b984722d1.png)




        program 24:2. Program to perform basic image manipulation:
                   a) Sharpness
                    b) Flipping
                   c) Cropping
                   
                   
         from PIL import Image
         from PIL import ImageFilter
         import matplotlib.pyplot as plt
         my_image=Image.open('images (3).jpg')
         sharp=my_image.filter(ImageFilter.SHARPEN)
         sharp.save('D:/image.sharpen.jpg')
         sharp.show()
         plt.imshow(sharp)
         plt.show()
         
 ![image](https://user-images.githubusercontent.com/19484531/179955355-b6c2db2a-8571-4dcb-956c-8ba2d8b3955a.png)

        
        
          import matplotlib.pyplot as plt
          img=Image.open('images (3).jpg')
          plt.imshow(img)
          plt.show()
          flip=img.transpose(Image.FLIP_LEFT_RIGHT)
          flip.save('D:/image_flip.jpg')
          plt.imshow(flip)
         plt.show()
         
         
 ![image](https://user-images.githubusercontent.com/19484531/179955518-56bb5255-503c-4eec-b9b3-7ee1fb74b676.png)
 
 -----------------------------------------------------------------------------------------------------------------------------
 
           D-Drive:
           
 ![image](https://user-images.githubusercontent.com/19484531/179956477-097b41b4-3112-47df-828a-3535094864fb.png)

------------------------------------------------------------------------------------------------------------------------------

          from PIL import Image
          import matplotlib.pyplot as plt
          im=Image.open('images (3).jpg')
          width,height=im.size
          im1=im.crop((40,50,200,150))
          im1.show()
          plt.imshow(im1)
          plt.show()
          
 ![image](https://user-images.githubusercontent.com/19484531/179955667-ca47ddbf-1852-4332-87b4-ba69ce7a62c3.png)


         program 24:

        import numpy as np
        import matplotlib.pyplot as plt

        arr = np.zeros((256,256,3), dtype=np.uint8)
        imgsize = arr.shape[:2]
        innerColor = (255, 255, 255)
        outerColor = (10,10,10)
       for y in range(imgsize[1]):
           for x in range(imgsize[0]):
             #Find the distance to the center
                  distanceToCenter = np.sqrt((x - imgsize[0]//2) ** 2 + (y - imgsize[1]//2) ** 2)

        #Make it on a scale from 0 to 1innerColor
                  distanceToCenter = distanceToCenter / (np.sqrt(2) * imgsize[0]/2)

        #Calculate r, g, and b values
        r = outerColor[0] * distanceToCenter + innerColor[0] * (1 - distanceToCenter)
        g = outerColor[1] * distanceToCenter + innerColor[1] * (1 - distanceToCenter)
        b = outerColor[2] * distanceToCenter + innerColor[2] * (1 - distanceToCenter)
        # print r, g, b
        arr[y, x] = (int(r), int(g), int(b))

        plt.imshow(arr, cmap='gray')
       plt.show()
       
       
 ![image](https://user-images.githubusercontent.com/19484531/180202842-29d37fe4-661c-4711-910d-79b3c7a52af3.png)

 
 
           program 25:
          from PIL import Image
          import numpy as np
          import matplotlib.pyplot as plt
           w, h = 500, 512
          data = np.zeros((h, w, 3), dtype=np.uint8)


         data[220:320, 220:320] = [255, 255,255]
           data[320:420, 320:420] = [180, 180,180]
          data[0:120, 0:120] = [120, 120,120]
         data[120:220, 120:220] = [120, 120,120]
          data[420:512, 420:512] = [255, 255,255]
        # red patch in upper left
          img = Image.fromarray(data, 'RGB')
          img.save('rose7.jpg')
         img.show()
          plt.imshow(img)
       
       
 ![image](https://user-images.githubusercontent.com/19484531/180203271-aca00ac0-15ed-420f-9ce7-b6d21cc053e3.png)



       pattern:

       # Python3 program for printing
       # the rectangular pattern
 
       # Function to print the pattern
        def printPattern(n):
 
          arraySize = n * 2 - 1;
              result = [[0 for x in range(arraySize)]
                 for y in range(arraySize)];
         
         # Fill the values
            for i in range(arraySize):
              for j in range(arraySize):
                  if(abs(i - (arraySize // 2)) >
                    abs(j - (arraySize // 2))):
                    result[i][j] = abs(i - (arraySize // 2));
            else:
                result[i][j] = abs(j - (arraySize // 2));
             
    # Print the array
    for i in range(arraySize):
        for j in range(arraySize):
            print(result[i][j], end = " ");
        print("");
 
    # Driver Code
     n = 4;
 
     printPattern(n);


 ![image](https://user-images.githubusercontent.com/19484531/181234717-211380c5-e061-4f62-90f6-fb4ffbe5727c.png)


      average,standard deviation,minimum and maximum pixel values
      
      import imageio
       import matplotlib.pyplot as plt
      img=imageio.imread("bird1.jpg")
      plt.imshow(img)
      np.average(img)
      
 ![image](https://user-images.githubusercontent.com/19484531/181235159-f18b1290-5ed2-4b47-97aa-2dce32059047.png)
 
      from PIL import Image,ImageStat
     import matplotlib.pyplot as plt
     im=Image.open('bird1.jpg')
     img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
     plt.imshow(im)
     plt.show()
     stat=ImageStat.Stat(im)
     print(stat.stddev)
![image](https://user-images.githubusercontent.com/19484531/181235253-25610edf-0cbb-4608-a81f-82e3230302ae.png)


     import imageio
     import numpy as np
     import matplotlib.pyplot as plt
     img=imageio.imread('bird1.jpg' )
     plt.imshow(img)
     plt.show()
     max_channels = np.amax([np.amax(img[:,:,0]), np.amax(img[:,:,1]),np.amax(img[:,:,2])])

     print(max_channels)
     
     
 ![image](https://user-images.githubusercontent.com/19484531/181235362-2cbaf32a-49d9-4b80-b9fa-323d7f78d57a.png)


     import imageio
      import numpy as np
      import matplotlib.pyplot as plt
      img=imageio.imread('bird1.jpg' )
      plt.imshow(img)
      plt.show()
      min_channels = np.amin([np.min(img[:,:,0]), np.amin(img[:,:,1]),np.amin(img[:,:,2])])

      print(min_channels)
      
      
 ![image](https://user-images.githubusercontent.com/19484531/181235454-b8178ea8-6c90-4016-8505-b83dfa5d6e0f.png)



25) Pillow library

                    from PIL import Image,ImageChops,ImageFilter
                    from matplotlib import pyplot as plt
                    x=Image.open("x.png")
                    o=Image.open("o.png")
                    print('size of the image:',x.size,'colour mode:',x.mode)
                    print('size of the image:',o.size,'colour mode:',x.mode)
                    plt.subplot(121),plt.imshow(x)
                    plt.axis('off')
                    plt.subplot(122),plt.imshow(o)
                    plt.axis('off')
                    merged=ImageChops.multiply(x,o)
                    add=ImageChops.add(x,o)
                    grayscale=merged.convert('L')
                    grayscale
                    
                    
                    out put:
                    size of the image: (256, 256) colour mode: RGB
                    size of the image: (256, 256) colour mode: RGB
                    
 ![image](https://user-images.githubusercontent.com/19484531/186652629-3537031c-4528-423d-bde1-94548d9db2ea.png)

             image=merged
                             print('image size:',image.size,'\ncolour mode:',image.mode,'\nImage width:',image.width,'| also represented by :',image.size[0],'\nImage                 height',image.height,'| also represented by:',image.size[1])                      
                             
                       
               output:
               image size: (256, 256) 
                colour mode: RGB 
                Image width: 256 | also represented by : 256 
                Image height 256 | also represented by: 256
                
           pixel=grayscale.load()
            for row in range(grayscale.size[0]):
                for column in range(grayscale.size[1]):
                    if pixel[row,column]!=(255):
                        pixel[row,column]=(0)
            grayscale
            
 ![image](https://user-images.githubusercontent.com/19484531/186652881-1b98ae97-ad02-49f2-b84e-bbad1449b072.png)
 
 
             Invert=ImageChops.invert(grayscale)
            bg=Image.new('L',(256,256),color=(255))
            subt=ImageChops.subtract(bg,grayscale)
            rotate=subt.rotate(45)
            rotate
![image](https://user-images.githubusercontent.com/19484531/186652956-12888c2d-4264-46ea-b333-35708e8189a5.png)

            blur=grayscale.filter(ImageFilter.GaussianBlur(radius=1))
            edge=blur.filter(ImageFilter.FIND_EDGES)
            edge
            
 ![image](https://user-images.githubusercontent.com/19484531/186653023-0d62a735-8bd9-40fd-a45d-5fa7b4643458.png)
 
 
             edge=edge.convert('RGB')
            bg_red=Image.new('RGB',(256,256),color=(255,0,0))
            filled_edge=ImageChops.darker(bg_red,edge)
            filled_edge
            
  ![image](https://user-images.githubusercontent.com/19484531/186653097-f1df8986-9914-4d89-9f6e-6d67e340ec81.png)


            edge.save('processed.png')
            
            
 ![image](https://user-images.githubusercontent.com/19484531/186653388-8bdf1007-8230-4384-b0b2-bab2dcfd23c9.png)


26) lab exersize:

                 import numpy as np
                import cv2
                import matplotlib.pyplot as plt
                #open the image
                img=cv2.imread('dimage_damaged.png')
                plt.imshow(img)
                plt.show()
                #load the mask
                mask=cv2.imread('dimage_mask.png',0)
                plt.imshow(mask)
                plt.show()
                #inpaint
                dst=cv2.inpaint(img,mask,3,cv2.INPAINT_TELEA)
                #write output
                cv2.imwrite('dimage_inpainted.png',dst)
                plt.imshow(dst)
                plt.show()
                
 ![image](https://user-images.githubusercontent.com/19484531/186653594-7a58af78-1e9d-472f-9405-9f9680c1e568.png)
 
           import numpy as np
            import matplotlib.pyplot as plt
            import pandas as pd
            plt.rcParams['figure.figsize']=(10,8)
            
                      def show_image(image,title='Image',cmap_type='gray'):
                plt.imshow(image,cmap=cmap_type)
                plt.title(title)
                plt.axis('off')
            def plot_comparison(img_original,img_filtered,img_title_filtered):
                fig,(ax1,ax2)=plt.subplots(ncols=2,figsize=(10,8),sharex=True,sharey=True)
                ax1.imshow(img_original,cmap=plt.cm.gray)
                ax1.set_title('Original')
                ax1.axis('off')
                ax2.imshow(img_filtered,cmap=plt.cm.gray)
                ax2.set_title(img_title_filtered)
                ax2.axis('off')

                from skimage.restoration import inpaint
                from skimage.transform import resize
                from skimage import color
                
                
                image_with_logo=plt.imread('imlogo.png')
                    #initialize mask
                    mask=np.zeros(image_with_logo.shape[:-1])
                    #set the pixel where the logo is to 1
                    mask[210:272,360:425]=1
                    #apply inpainting to remove the logo
                    image_logo_removed=inpaint.inpaint_biharmonic(image_with_logo,mask,multichannel=True)
                    #show both the image
                    plot_comparison(image_with_logo,image_logo_removed,'Image with logo removed')
                    
![image](https://user-images.githubusercontent.com/19484531/186653815-22f97e6a-5aaa-44b6-9234-d637847b1f48.png)



                from skimage.util import random_noise
                fruit_image=plt.imread('fruitts.jpeg')
                noisy_image=random_noise(fruit_image)
                plot_comparison(fruit_image,noisy_image,'Noisy image')
                
 ![image](https://user-images.githubusercontent.com/19484531/186653878-4259d311-8890-4876-95db-9820570d4251.png)
 
 
                 from skimage.restoration import denoise_tv_chambolle
                noisy_image=plt.imread('noisy.jpg')
                denoised_image=denoise_tv_chambolle(noisy_image,multichannel=True)
                plot_comparison(noisy_image,denoised_image,'Denoised Image')
                
   ![image](https://user-images.githubusercontent.com/19484531/186653967-11b4de6f-cdc2-4687-b118-e084ef455a07.png)
   

                   from skimage.restoration import denoise_bilateral
                landscape_image=plt.imread('noisy.jpg')
                denoised_image=denoise_bilateral(landscape_image,multichannel=True)
                plot_comparison(landscape_image,denoised_image,'Denoised Image')
                
                
   ![image](https://user-images.githubusercontent.com/19484531/186654060-627d2c7d-0ef2-4367-8d7d-1d591148661e.png)
   

                   from skimage.segmentation import slic 
                from skimage.color import label2rgb
                face_image = plt.imread('face.jpg')
                # obtain the segmentation with 400 regions 
                segments = slic(face_image,n_segments=400)
                # Put segments on top of original image to compare
                segmented_image =label2rgb(segments, face_image, kind='avg')
                #Show the segmented image
                plot_comparison (face_image, segmented_image, 'Segmented image, 400 superpixels')
                
                
         or
         
         
                    from skimage.segmentation import slic
                    from skimage.color import label2rgb
                    import matplotlib.pyplot as plt
                    import numpy as np
                    face_image = plt.imread('face.jpg')
                    segments = slic(face_image, n_segments=400)
                    segmented_image=label2rgb(segments,face_image,kind='avg')
                    plt.imshow(face_image)
                    plt.show()
                    plt.imshow((segmented_image * 1).astype(np.uint8))
                    plt.show()
                
  ![image](https://user-images.githubusercontent.com/19484531/186654269-30ee002a-de75-45de-93f1-3619c5b59525.png)
  
  
  
                   def show_image_contour(image, contours):
                    plt.figure()
                    for n, contour in enumerate (contours):
                        plt.plot(contour[:, 1], contour[:,0], linewidth=3)
                    plt.imshow(image, interpolation='nearest',cmap='gray_r')
                    plt.title('contours')
                    plt.axis('off')
                    
                    
                    from skimage import measure,data
                    horse_image=data.horse()
                    contours=measure.find_contours(horse_image,level=0.8)
                    show_image_contour(horse_image,contours)
                    
                    
   ![image](https://user-images.githubusercontent.com/19484531/186654570-dc94ccee-e793-4fdd-a9a7-2e47cfd9fef6.png)
   
   
   
                   from skimage.io import imread
                from skimage.filters import threshold_otsu
                image_dices = imread('diceimg.png')
                # Make the image grayscale 
                image_dices = color.rgb2gray(image_dices)
                # Obtain the optimal thresh value 
                thresh = threshold_otsu(image_dices)
                # Apply thresholding 
                binary=image_dices > thresh
                # Find contours at a constant value of 0.8 
                contours = measure.find_contours (binary, level=0.8)
                # Show the image
                show_image_contour(image_dices, contours)
                
                
    ![image](https://user-images.githubusercontent.com/19484531/186654643-e8735bf5-dc64-4728-91b5-89fcbd678d6f.png)
    
    

                #Create List with the shape of each contour 
            shape_contours = [cnt.shape[0] for cnt in contours]
            # Set 50 as the maximum size of the dots shape 
            max_dots_shape=50
            #Count dots in contours excluding bigger than dots size 
            dots_contours = [cnt for cnt in contours if np.shape(cnt) [0] < max_dots_shape]
            #Shows all contours found 
            show_image_contour(binary, contours)
            #Print the dice's number
            print('Dices dots number:{}.'.format(len(dots_contours)))
            
            
![image](https://user-images.githubusercontent.com/19484531/186654719-553f09b2-c701-4b6d-888c-69ec125e8ba0.png)



**
 27) Implement a program to perform various edge detection techniques 
                a) Canny Edge detection
                import cv2
                import numpy as np 
                import matplotlib.pyplot as plt 
                plt.style.use('seaborn')
                loaded_image = cv2.imread("shape1.jpeg") 
                loaded_image = cv2.cvtColor(loaded_image,cv2.COLOR_BGR2RGB)
                gray_image = cv2.cvtColor(loaded_image,cv2.COLOR_BGR2GRAY)
                edged_image = cv2.Canny(gray_image, threshold1=30, threshold2=100)
                plt.figure(figsize=(20,20))
                plt.subplot(1,3,1)
                plt.imshow(loaded_image, cmap="gray") 
                plt.title("original Image")
                plt.axis("off")
                plt.subplot(1,3,2)
                plt.imshow(gray_image,cmap="gray")
                plt.axis("off")
                plt.title("GrayScale Image")
                plt.subplot(1,3,3)
                plt.imshow(edged_image, cmap="gray")
                plt.axis("off")
                plt.title("Canny Edge Detected Image")
                plt.show()

![image](https://user-images.githubusercontent.com/19484531/187897964-f84a4108-f8ea-47c3-b22a-f3eea6deaec7.png)


b) Edge detection schemes - the gradient (Sobel - first order derivatives)  based edge detector and the Laplacian (2nd order derivative, so it is  extremely sensitive to noise) based edge detector.

                import cv2
                import numpy as np 
                import matplotlib.pyplot as plt
                img0=cv2.imread("shape1.jpeg")
                gray=cv2.cvtColor(img0,cv2.COLOR_BGR2GRAY)
                img=cv2.GaussianBlur(gray,(3,3),0)
                laplacian=cv2.Laplacian(img,cv2.CV_64F)
                sobelx=cv2.Sobel(img,cv2.CV_64F,1,0,ksize=5)
                sobely=cv2.Sobel(img,cv2.CV_64F,0,1,ksize=5)

                plt.subplot(2,2,1),plt.imshow(img,cmap='gray')
                plt.title('Original'),plt.xticks([]),plt.yticks([])

                plt.subplot(2,2,2),plt.imshow(laplacian,cmap='gray')
                plt.title('Laplacian'),plt.xticks([]),plt.yticks([])

                plt.subplot(2,2,3),plt.imshow(sobelx,cmap='gray')
                plt.title('Sobel X'),plt.xticks([]),plt.yticks([])

                plt.subplot(2,2,4),plt.imshow(sobely,cmap='gray')
                plt.title('Sobel Y'),plt.xticks([]),plt.yticks([])
                plt.show()
                
![image](https://user-images.githubusercontent.com/19484531/187898068-746c7880-ce68-4029-89b3-0c08867d454b.png)

c) Edge detection using Prewitt Operator
                import cv2
                import numpy as np
                from matplotlib import pyplot as plt
                imge=cv2.imread("shape.jpg")
                gray=cv2.cvtColor(imge,cv2.COLOR_BGR2GRAY)
                img_gaussian=cv2.GaussianBlur(gray,(3,3),0)

                kernelx= np.array([[1,1,1], [0,0,0],[-1,-1,-1]])
                kernely=np.array([[-1,0,1], [-1,0,1],[-1,0,1]])

                img_prewittx = cv2.filter2D(img_gaussian, -1, kernelx)
                img_prewitty = cv2.filter2D(img_gaussian, -1, kernely)

                cv2.imshow("Original Image", img)
                cv2.imshow("Prewitt x", img_prewittx) 
                cv2.imshow("Prewitt y", img_prewitty)
                cv2.imshow("Prewitt", img_prewittx + img_prewitty)
                cv2.waitKey()
                
  ![image](https://user-images.githubusercontent.com/19484531/187898258-a4f406cf-3e13-4721-b126-4d7de34ca3b3.png)


d) Roberts Edge Detection- Roberts cross operator


            import cv2
            import numpy as np
            from scipy import ndimage
            from matplotlib import pyplot as plt
            roberts_cross_v=np.array([[1,0],[0,-1]])
            roberts_cross_h=np.array([[0,1],[-1,0]])
            img=cv2.imread("shape.jpg",0).astype('float64')
            img/=255.0
            vertical=ndimage.convolve(img,roberts_cross_v)
            horizontal=ndimage.convolve(img,roberts_cross_h)

            edged_img=np.sqrt(np.square(horizontal)+np.square(vertical))
            edged_img*=255
            cv2.imwrite("output.jpg",edged_img)
            cv2.imshow("OutputImage",edged_img)
            cv2.waitKey()
            cv2.destroyAllWindows()
            
            
 ![image](https://user-images.githubusercontent.com/19484531/187898372-3192011c-e666-4666-a7b8-42ff18a6e85d.png)


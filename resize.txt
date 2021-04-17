#importing libraries 
from PIL import Image
import glob

#creating empty list for storing multiple images
image_list = []
resized_image = []
#appending all the images in to the list 
for filename in glob.glob("D:/imageprossing/*.jpg") :
    img = Image.open(filename)
    image_list.append(img)
    
#resized all images
for image in image_list:
    image = image.resize((500,500))
    resized_image.append(image)

    
#save images in to new folder 
for (i,new) in enumerate(resized_image):
    new.save("{}{}{}".format("C:/Users/PRIYANKA/Desktop/image processing/image",i+1,".png"))
    

--> Starts with importing librarie "ImageEnhance" claas from "PIL" module used to enhance the brightness of images.

--> The background image and main image are both saved in jpeg format. Use Image.open("file name") to open these images.

--> Both main image and background brightness is increased. This is done with "ImageEnhance.Brightness" class to create an enhancer object, and then the "enhance()" method is called with a 
    brightness factor to adjust the brightness level.

--> background image is resized to match size of main image using Lanczos interpolatio. This ensures that both images have same dimensions.

--> main image and background image are converted to RGBA mode which includes an alpha channel for transparency

--> shadow effect is created by reducing the opacity of the main image. This is for creating a copy of the main image "shadow_image" and then setting the alpha channel values to reduce the 
    opacity

--> mask is created for shadow by extracting the alpha channel from the main image and pasting it onto a new image (shadow_mask). is used to control the transparency of the shadow when     
    overlaying it onto the background

--> background of the main image is replaced with the new background image this is done by creating a copy of the main image without its background and then pasting the background image 
    onto it using the alpha channel of the main image as a mask

--> main image without its background and the shadow image are overlaid onto the new background using alpha compositing. this blends the image together taking into account their 
    transparency values.

--> and the image is saved as "product_4_1.png" with a quality level.

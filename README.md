# Stable Diffusion Inpainting-Tutorial
Some tips on using stable diffusion inpainting with diffusers.

Try it out directly in GoogleColab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]([https://colab.research.google.com/github/weiji14/deepbedmap/](https://github.com/Markus-Pobitzer/Inpainting-Tutorial/blob/main/InpaintingTutorial.ipynb)https://github.com/Markus-Pobitzer/Inpainting-Tutorial/blob/main/InpaintingTutorial.ipynb)

## Inpainting with Stabilityai pipeline
How to Inpaint an Image and corresponding mask with Stable Diffusion

![Inpainting with StabilityAIs model](https://raw.githubusercontent.com/Markus-Pobitzer/Inpainting-Tutorial/main/imgs/StabilityaiInpainting.png)

## Keep the original image in the unmasked area
Maybe you have noticed it, there are small changes to the unmasked area of the inpainted image (i.e. bench). The part of the image that should not have changed got slightly modified. 

The solution: use the original image and put the inpainted part on it. This means we will blend the two images together.

![Inpainting with StabilityAIs model](https://raw.githubusercontent.com/Markus-Pobitzer/Inpainting-Tutorial/main/imgs/OriginalBackground.png)


## Change of background
With the presented model it is easy to change the background of an image as long as we have the corresponding mask.

![Inpainting with StabilityAIs model](https://raw.githubusercontent.com/Markus-Pobitzer/Inpainting-Tutorial/main/imgs/BottleMask.png)


Sometimes it can happen, that the object in the foreground gets continued by the model. This may be an unwanted effect (as seen in the next image on the left). To mitigate this problem we will see two workarounds.


![Inpainting with StabilityAIs model](https://raw.githubusercontent.com/Markus-Pobitzer/Inpainting-Tutorial/main/imgs/BottleVariations.png)

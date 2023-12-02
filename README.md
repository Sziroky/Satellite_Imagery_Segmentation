# Satellite_Imagery_Segmentation

Do you ever wanted to perform automated segmentation on satellite imagery. With this Google Colab project I want to give you a hands on and understanding of segmentation tasks on satellite imagery. This notebook is based on Prodramp workshops: Deep learning Workshop for Satellite Imagery. But it's not only the bare code. I tried to explain methods models etc. inside the code so You would better understand what's going on why I chosed this metric how the dimension looks like. 
What I want to do next is change the infrastructure of U-NET according to papers like "Detection of Surface Crevasses over Antarctic Ice Shelves Using SAR Imagery and Deep Learning Method" of scientist from University of Chinese Academy of Sciences, articles: "Satellite Image Segmentation: a Workflow with U-Net" and other resources like github repository of Alex-Mathai-98: "Satellite-Image-Segmentation-Using-U-NET". Hope you find it helpfull!  

# Dataset
For this colab I use Kaggle dataset: https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery 
This Dataset consist 8 tiles that were cropped into 9 images each. In total 72 images. 
This images was captured by MBRSC satellites in Dubai.
For every image there is a mask that provide pixel-wise class of the target.

#Procesing of the images
There are two main steps to proces the images. 
First is to crop them into patches because we need to have all images in the same size.
Second is to normalize the pixel values from <0:255> to <0:1>. We perform it using MinMaxScaler.
After these two steps there are 945 images each of the shape(256x256x3) and values between <0:1>,

# Procesing of the masks

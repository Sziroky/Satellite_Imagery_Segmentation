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

# Procesing of the masks.
The masks also need to be proceed. First they must be the same size as the patched image. And also the colors need to be converted into classes. After that I perform one-hot encoding for binary representation of classes.

#U-NET
In this Colab Notebook we recreate the original U-NET but we change number of filters. Future things i want to do is to check the performance of diffrent U-NEts according to research and aplications in Satellite imagery.

#Summary.
Check this notebook if you: Want a hands-on in deep learning, want to get to know step by step explaination of how to perform deep learning on satellite imagery. Also i very recomend watching great videos from mr. Avkash Chauhan.

#Sources:
Avkash Chauhan Prodramp workshops:
Repository: https://github.com/prodramp/DeepWorks/tree/main/DL-SatelliteImagery
YouTube: https://youtu.be/3Xn21RT-y7Y?si=woavf8syHg2lfARp
Kaggle dataset: https://www.kaggle.com/datasets/humansintheloop/semantic-segmentation-of-aerial-imagery


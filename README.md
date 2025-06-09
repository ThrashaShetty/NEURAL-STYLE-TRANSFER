## NEURAL-STYLE-TRANSFER

"COMPANY": CODETECH IT SOLUTIONS

"NAME": THRASHA SHETTY

"INTERN ID": CT04DN376

"DOMAIN": ARTIFICIAL INTELLIGENCE

"DURATION": 4 WEEKS

"MENTOR": NEELA SANTHOSH

## TASK DESCRIPTION

This Python project implements Neural Style Transfer using PyTorch, allowing you to blend the *content of one image* with the artistic style of another. It uses a pre-trained VGG19 convolutional neural network to extract high-level visual features from both the content and style images. The process begins by loading and preprocessing the input images, extracting features from specific layers of the network, and computing style representations using Gram matrices. The goal is to generate a new target image that preserves the structure of the content image while adopting the textures, colors, and brushstroke patterns of the style image.

The target image is initialized as a copy of the content image and is gradually optimized through backpropagation. A weighted combination of content loss and style loss is used to guide the training process over many iterations. The optimizer adjusts the pixels of the target image to minimize this loss, effectively blending the content and style. The final result is a visually striking, stylized image that is saved to disk. This application demonstrates how deep learning can be used creatively for image synthesis and digital art.

How it works: 
1. Image Loading & Preprocessing:
     The content and style images are loaded using PIL.
     They are resized and normalized using the same mean and standard deviation as the VGG19 model's training on ImageNet.
     This prepares them to be input into the neural network.

2.Model Setup (VGG19):
     A pre-trained VGG19 model (feature extractor) is loaded from torchvision.models.
     Only the convolutional layers (.features) are used.
     The model is frozen (no training) since we only use it to extract features

3. Feature Extraction:
    Specific layers of VGG19 are chosen to extract:
    Content features (from deeper layer conv4_2)
    Style features (from multiple shallow and deep layers like conv1_1, conv2_1, etc.)
   
4.Style Representation: Gram Matrix:
    For each style layer, a Gram Matrix is computed from its features.
    The Gram matrix captures correlations between filter responses — this represents texture and style.

5.Target Image Initialization:
    The target image starts as a copy of the content image.
    It is the image we will optimize, by changing its pixel values, to match both the style and content.

6.Loss Calculation:  
    Content Loss: Measures the difference between the target and content image’s features.
    Style Loss: Measures the difference between the target and style Gram matrices.
    The total loss is a weighted sum of both.

7.Optimization:
    The target image is updated using Adam optimizer to minimize the total loss.
    Over multiple iterations, the image gradually transforms to combine the content and style characteristics.
  
8.Postprocessing & Saving:
    The final target tensor is denormalized and converted back to a PIL image.
    The stylized image is saved to disk as the output.
    
Key feature:The key features of this Neural Style Transfer project include the ability to combine any two images—one for content and one for style—to generate a new, artistic output. It leverages a pre-trained VGG19 model for deep feature extraction, ensuring high-quality and detailed style rendering. The application is GPU-accelerated for faster processing and allows customization through adjustable content and style weights, as well as iteration count. It also includes real-time progress logging, image preprocessing and postprocessing utilities, and automatically saves the final stylized image. These features make the tool both powerful and flexible for creative image synthesis.

Applications:Neural Style Transfer has a wide range of creative and practical applications across various fields. In digital art and design, artists use it to generate stylized artwork by blending classical painting styles with modern photographs. It is also popular in photo editing and filters, where apps apply artistic effects to user images in real time. In film and animation, it helps in creating consistent visual themes by applying a specific style across multiple frames or scenes.

     Beyond entertainment, Neural Style Transfer finds applications in advertising, branding, and fashion, where unique visual aesthetics are important. It is also used in AI-assisted creativity tools, allowing users with no artistic background to produce visually rich and customized artwork. Additionally, it's useful in AR/VR environments for creating immersive, stylized scenes. Overall, it bridges the gap between deep learning and human creativity.

This Neural Style Transfer project demonstrates the powerful synergy between deep learning and artistic creativity. By leveraging a pre-trained VGG19 model, the code effectively captures the structural content of one image and the artistic style of another, blending them into a visually compelling output. With its flexibility, GPU support, and customizable parameters, the application offers both a technical and artistic tool for creating unique, stylized images.

## OUTPUT

![Image](https://github.com/user-attachments/assets/703300d7-7c99-4f06-af49-c7bff8733139)

![Image](https://github.com/user-attachments/assets/0eca9f59-ca31-4ac9-8f4b-302d6d791ccf)










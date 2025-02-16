# Generative-Models

In this work, we introduce a reverse engineering pipeline designed to recover original text
prompts used to generate images. By leveraging advanced machine learning models, our
approach seeks to bridge the gap between text-to-image generation and image caption
generation, improving the similarity of AI-generated image captions to its original descriptive
texts.
We present a pipeline that consists of two components. Initially, selected prompts are
processed through the first component, the Stable Diffusion v2-base model, to create
AI-images based on these input sentences. These images serve as inputs to the second
component, the BLIP captioner, which generates captions from the images, aiming to
recreate the original text prompts as closely as possible. This research involves training the
BLIP captioner to minimize the language modelling loss between the generated captions
and the actual prompts, therefore improving its ability to recover the original descriptive
text only from the generated images.
We used for evaluation a preprocessed subset of a fashion product dataset, a dataset
available on Kaggle, which contains a description-image pairs of fashion articles. Our
findings indicate a significant improvement in the similarity between generated captions
and original prompts after training, with a notable increase in the average similarity score
of the input-output sentences pairs. Further, our analysis shows that images generated
from fine-tuned captions are highly comparable to prompt-based AI-images as well as to
real-world images of the fashion products.
We also observed challenges such as information loss during multiple pipeline iterations,
where the focus of generated content gradually shifts away from the original prompts, This
effect also extends to the synthesized images conditioned on those generated descriptions,
leading to deviations from the intended visual output.

#Architecture 
![inference](https://github.com/user-attachments/assets/8ce2495d-7fb7-4ff0-ba81-304a9b8bfcb8)

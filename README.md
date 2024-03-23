# DL-CycleGAN-Monet2Photo
## Overview
This project was carried out as part of "I’m Something of a Painter Myself" competition on the Kaggle website. The project presents a CycleGAN model with Kaggle's MiFID score of 67, whose function is to convert normal photos into Monet-style images. The task of transforming photographs into Monet-style paintings is an example of unpaired image-to-image translation. In this case, the goal is to convert everyday photographs into images that capture the distinct visual characteristics of Monet's paintings, such as vibrant colors, textured brushstrokes, and dreamy atmospheres.

CycleGAN achieves this transformation by simultaneously training two generators and two discriminators. The generators learn to translate images from one domain (photographs) to another (Monet-style paintings), while the discriminators distinguish between real and generated images. Through adversarial training and cycle-consistency loss, CycleGAN ensures that the translated images not only resemble the target style but also preserve the content of the original photographs.

It should be noted that the size of the images that enter this model is 320 x 320 (as opposed to the common approach of using 256 x 256 size images) and that the receptive field size of the discriminator is different from 70 x 70 by definition. These changes were included in the project to increase its level of difficulty and to try to prevent direct use of projects found on the Internet.

Each notebook has a different purpose. The test notebook was designed to see the final model and insert an image into it, in order to translate it to a different domain, while the training notebook was created to understand the improvement process that was carried out in the project, the examination of the various structures that were used and the conclusions that led to the final model.

## Data Preparation
1. The Kaggle API was utilized to download the dataset efficiently.
2. Split action took place in cases where the model was trained with fewer than 300 images for each domain.
3. Scaled all images to a pixle range of [-1, 1].
4. Resized all images to a size of 320x320.
5. Normalization operation.

## Improvements Process
The training notebook consists all explanations and conclusions about how the best result was achieved. 

## Setup
1. Open and save a copy of the Google Colab notebooks in your Google Drive.
3. Open a Kaggle account and create an API token for fetching the dataset (or download the data to your local device and change the code accordingly). 
2. Check all paths within the code and make them suitable for your personal use.
4. Modify and train the models as you please.
5. A link to the trained model components is located in the test notebook.  

## Acknowledgments
* The project dataset is hosted by Kaggle and can be accessed by joining the competition "I’m Something of a Painter Myself".
* During the project, the Google Collab platform was used to gain access to GPU's in order to train the various models.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Feel free to contribute by opening issues or creating pull requests.

## Author
[UriB1](https://github.com/UriB1)

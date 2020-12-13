# Pix2Pix-Image-Video-Colourizing
### Using Pix2Pix Conditional GAN architecture to colourize image using Places365 dataset and use that model to colourize video clips

## Dataset
The Places365 dataset contains 1.8 million train images from 365 scene categories for varying sizes. 2000 images were used to train and 500 were used to test the Pix2Pix network. We resized the train and test images to size 256 x 256 x3. Then we created the corresponding grayscale images using a grayscale function which converted the image dimensions to 256 x 256 x1. 

## Video 
We took 2 videos. One was a 5 min clip from ‘The Great Dictator’, a black and white Charlie Chaplin movie and another was a 1 min colored video clip from YouTube which showed different sceneries.
•	The frames of the videos were extracted as jpg at a rate of 20 frames per second using VLC player
•	The extracted images were converted to NumPy arrays and fed to the trained generator to colorize. The color video frames were gray-scaled before being fed to the generator.
•	The output of the generator was combined again using matplotlib to obtain a video and it was analyzed.

# Training 
We can observe from figure that from epoch 6, the GAN has learned to identify the sky and color it blue. As the training progresses, it learns to color grass and trees green and other outdoor cues.




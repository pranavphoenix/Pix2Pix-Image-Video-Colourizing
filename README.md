# Pix2Pix-Image-Video-Colourizing
### Using Pix2Pix Conditional GAN architecture to colourize image using Places365 dataset and use that model to colourize video clips

## Dataset
The Places365 dataset contains 1.8 million train images from 365 scene categories for varying sizes. 2000 images were used to train and 500 were used to test the Pix2Pix network. We resized the train and test images to size 256 x 256 x3. Then we created the corresponding grayscale images using a grayscale function which converted the image dimensions to 256 x 256 x1. 

## Video 
We took 2 videos. One was a 5 min clip from ‘The Great Dictator’, a black and white Charlie Chaplin movie and another was a 1 min colored video clip from YouTube which showed different sceneries.
- The frames of the videos were extracted as jpg at a rate of 20 frames per second using VLC player
- The extracted images were converted to NumPy arrays and fed to the trained generator to colorize. The color video frames were gray-scaled before being fed to the generator.
- The output of the generator was combined again using matplotlib to obtain a video and it was analyzed.

# Training 
We can observe from figure that from epoch 6, the GAN has learned to identify the sky and color it blue. As the training progresses, it learns to color grass and trees green and other outdoor cues. 
###### Top row grayscale image input, middle row is generated image by GAN, last row is actual image

### Epoch 1
![plot_000001](https://user-images.githubusercontent.com/15833382/102006410-eb52a880-3d46-11eb-8d81-f96685cb90e8.png)
### Epoch 6
![plot_000006 (1)](https://user-images.githubusercontent.com/15833382/102006469-5603e400-3d47-11eb-9036-2fc28e08acba.png)
### Epoch 11
![plot_000011 (1)](https://user-images.githubusercontent.com/15833382/102006472-5b612e80-3d47-11eb-832f-ae2a940d1f67.png)
### Epoch 16
![plot_000016 (1)](https://user-images.githubusercontent.com/15833382/102006480-61efa600-3d47-11eb-8676-be403c2cef7f.png)
### Epoch 21
![plot_000021](https://user-images.githubusercontent.com/15833382/102006484-66b45a00-3d47-11eb-91ee-dae19fffa607.png)
### Epoch 26
![plot_000026](https://user-images.githubusercontent.com/15833382/102006486-6a47e100-3d47-11eb-80a1-54bd3f8808ba.png)
### Epoch 31
![plot_000031](https://user-images.githubusercontent.com/15833382/102006488-6f0c9500-3d47-11eb-9e09-921a77890e60.png)
### Epoch 36
![plot_000036](https://user-images.githubusercontent.com/15833382/102006489-72a01c00-3d47-11eb-9792-4efee41a5dbf.png)
### Epoch 41
![plot_000041](https://user-images.githubusercontent.com/15833382/102006491-7895fd00-3d47-11eb-96a9-5c44552654a3.png)
### Epoch 46
![plot_000046](https://user-images.githubusercontent.com/15833382/102006495-7c298400-3d47-11eb-8732-e6165098609b.png)

Figure shows an interesting case we observed while testing the GAN model, even though the input grayscale image or actual image showed a dark silhouette of a house, the model filled in the details it learned from trained by putting a window and door and lightening the image. Even the ground and sky are colored correctly. 






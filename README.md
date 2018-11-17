# MLF_Grayscale_Image_Colorization
Automatic colorization of grayscale images to output RGB images

The project intends to realize automatic colorization of grayscale images. Workflows of the project is as follows.

![flowchart]('./flowchart.png')

The CNN model employed here utilizes the structure of a ResNet18 model. First half of the model is transplanted from the first six layers of a ResNet18 model, so as to extract mid-level features of an image. Second half of the model is upsampling. For more details, please visit Luke Melas-Kyriazi's homepage(https://lukemelas.github.io/). The model here modifies Luke's model with respect to   
+ definition of parsers: args.epochs is a parameter for number of epochs in a call of main(), not the index for maximum epochs in a call.
+ save checkpoints: save the best model only.
+ validation: plot log losses against epochs to have a better visulization of validation performance. MSE loss is used. 

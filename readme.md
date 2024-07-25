# Ice Cream Bing Chilling AI

My project can classify two types of dessert for restaurants: ice cream cones and popsicles. This tool could be used by ice cream trucks, restaurants, and consumers who need to sort their desserts.
![Strawberrry-ice-cream-cone-250](https://github.com/user-attachments/assets/01770a16-c2cc-4dd2-be63-aa373ee19edb)
an ice cream cone

![Rainbow-Popsicles-Landscape-500x500](https://github.com/user-attachments/assets/66d537ba-1539-488c-b42b-8c8b2d60fcfd)
popsicle


## The Algorithm

My project works by training a neural network on images of ice cream cones and popsicles. I retrained resnet-18 imagenet on the Jetson Nano. I ran the training for several hours until test accuracy was consistently over 95%.

## Running this project

1. Clone dusty-nv's jetson-inference libary using the command `git clone --recursive https://github.com/dusty-nv/jetson-inference`
2. Navigate to the /home/nvidia/jetson-inference/python/training/classification
3. After putting the dataset in /jetson-inference/python/training/classification/data and the model in /jetson-inference/python/training/classification/models, set bash enviorment variables "NET=models/ice_cream" and "DATASET = data/ice_cream"
4. Run the command `imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/(name of class)/(image from class directory).jpg (where it will be saved.jpg)`
5. Look in the terminal output to see the classification and confidence level of the input image

[View a video explanation here](video link)

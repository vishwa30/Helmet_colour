# Helmet_colour_detection
This repo is to identify the type/colour of hard helmet which is generally used in industial plants.

## Dataset
Dataset used to test this is hard hat dataset from kaggle.
https://www.kaggle.com/andrewmvd/hard-hat-detection

## Sample output
The sample output images are saved in sample_dataset/output.
The sample images and annotations are also present in sample_dataset folder.

## Approch:
1. Taking one image which may contain the helmet.
2. Getting the bbox of all the classes ( Helmet,head ) for that image. Here using the xml file to extract bboxes. We can replace this by the trained model in future.  
3. Considering only the bboxes which are of label 'Helmet'.
4. Since the helmet annotation in the dataset is not just of helmet but of whole head of a person, therefore taking only the upper half portion of the face where the helmet will be present predominantly. Which inturn will help to remove the unwanted portion from the bbox.
5. Slicing the upper half portion and finding the dominant colours of this portion. (Helmet area)
6. Mathing this dominant colours from the color codes of Red,Blue,Yellow,Green and finding the colour distances.
7. Taking the colour from Red,blue,yellow,green which has the least colour distance and assigning this colour as the colour of helmet.
8. Putting text of the colour in the image and saving it in output file.
9. Printing the type of helmet according to the colour of helmet. 

## Running the code
1. To run the code download the dataset and save it in sample dataset folder.
2. Run the jupyter notebook.

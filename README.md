## Motivation: 

The primary motivation for this project is to generate descriptive captions for images which can be further used to retrieve images of similar categories from an image gallery. This idea will find applications in smartphones where our caption generator will create a single caption for each image in our phone image gallery. The user can then enter a key word or multiple key words ( for example: 'dog' and 'desk'), and our algorithm will return back all images whose generated caption contain the input key words. This feature allows for quick retrieval of images from a large gallery so that user need not manually locate specific images of interest.

### Project Deliverables

1. Creating descriptive captions for each image in our images gallery. 
2. A “Search” option that takes user input ( for eg. ‘dog on desk’ ) and returns all images from the images gallery whose captions contain those particular words. 

### Project Methodology 

We will be using Deep Learning to build this project. Following is a summary of the steps undertaken:
1. We used the (eg. Flickr30, MSCOCO) dataset which has images along with their captions. We will divide this dataset into train and test data.
2. Next, we checked if our data needs any cleaning. There was no cleaining needed.
3. We then vectorized all the images and the captions and then create a model that will train with the image vectors as features and the caption vectors as the target.
4. We also set a maximum limit for our captions so that our model would know where to stop.
5. The model mainly focused on providing the most probable word for every iteration, and for every iteration, we will be improving our sentence.
6. To improve the sentences, we processed the sequences using a Recurrent Neural network and predicted the index of the next word in a sentence.
7. For hyperparameter tuning, we used BLEU score to calculate the loss on a batch of data points to update the gradients.
8. Finally, began implementation by inputting the partial caption and the image vector to a feed-forward network(the model) which predicted the next word in the sequence of our caption.
9.In the end, we tested the model by passing new unobserved images and found the most probable captions for these images.

### Sample Predicted Captions

#### Image 1
<img src="prediction - flowers correct.JPG"/>

#### Image 2
<img src="https://github.com/megs161195/Image-Retrieval-using-generated-captions/raw/master/prediction%203-%20clock.JPG" alt ="Hi" class="inline"/>'

#### Image 3
<img src="https://github.com/megs161195/Image-Retrieval-using-generated-captions/raw/master/prediction%204_%20kite-sky.JPG" alt ="Hi" class="inline"/>'

#### Image 4
<img src="https://github.com/megs161195/Image-Retrieval-using-generated-captions/raw/master/prediction%205%20-%20correct%20cat.JPG" alt ="Hi" class="inline"/>'

#### Image 5
<img src="https://github.com/megs161195/Image-Retrieval-using-generated-captions/raw/master/prediction2-%20table%20with%20people%20eating%20food.JPG" alt ="Hi" class="inline"/>'

#### Image Retrieval Feature Using Keywords

---
driveId: 1Bqa_7uPthcROVROmCkRT3ekzXG2Eg6kq/preview
---

<iframe src="https://drive.google.com/file/d/1Bqa_7uPthcROVROmCkRT3ekzXG2Eg6kq/preview" width="640" height="480"></iframe>

{% include googleDrivePlayer.html id=page.driveId %}

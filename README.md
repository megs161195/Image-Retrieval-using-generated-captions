## Motivation: 

The primary motivation for this project is to generate descriptive captions for images which can be further used to retrieve images of similar categories from an image gallery. This idea will find applications in smartphones where our caption generator will create a single caption for each image in our phone image gallery. The user can then enter a key word or multiple key words ( for example: 'dog' and 'desk'), and our algorithm will return back all images whose generated caption contain the input key words. This feature allows for quick retrieval of images from a large gallery so that user need not manually locate specific images of interest.

### Project Deliverables

1. Creating descriptive captions for each image in our images gallery. 
2. A “Search” option that takes user input ( for eg. ‘dog on desk’ ) and returns all images from the images gallery whose captions contain those particular words. 

### Project Methodology 

We will be using Deep Learning to build this project. Following is a summary of the steps undertaken:
1. We use the MSCOCO dataset which has images along with their captions. We divide this dataset into train, validation, and test data.
2. Next, we check if our data needs any cleaning. There is no cleaining needed.
3. We then vectorize all the images and the captions and then build a model that will train with the image vectors as features and the caption vectors as the target.
4. We also set a maximum limit for our captions so that our model knows where to stop.
5. The model focuses on providing the most probable word for every iteration. After every iteration, the most probable word is added to the caption sentence.
6. To improve the accuracy of captions, we process the sequences using a Recurrent Neural network and predict the index of the next word in a sentence from our vocabulary.
7. For hyperparameter tuning, we use BLEU score as a metric to calculate the loss on a batch of data points and train the model until an optimun BLUE score value is reached.
8. Once the model is trained, we test the model performance by passing new unobserved images and predict the most probable captions for these images.

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
After every image is assigned one caption, you can retrieve the specific images you need by adding the words as keywords. The feature wil then retrieve all the images that have the keywords in their captions. 

The following video displays the working of the image retrieval feature.
We give two key words as input to our image retrieval algorithm- 'food' and 'table'. The result is all the images in our gallery whose generated captions contain those two keywords.

<iframe src="https://drive.google.com/file/d/1Bqa_7uPthcROVROmCkRT3ekzXG2Eg6kq/preview" width="640" height="480"></iframe>

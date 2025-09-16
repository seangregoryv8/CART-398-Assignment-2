## Overview
Our model is classifying different painting styles. Mainly Baroque, Renaissance, Realism and Medieval artstyles.
The dataset we are using is the ["WikiArt Art Movements/Styles"](https://www.kaggle.com/datasets/sivarazadi/wikiart-art-movementsstyles?select=Realism) available under public domain.

### Specs
1. Baroque (60 examples)
2. Renaissance (50 examples)
3. Realism (50 examples)
5. Mediaval (50 examples)
6. Face (23 examples)
7. None (19 examples)

The meta-parameters are 200 epochs, 16 size batch and 0.001 learning rate. Made using Google Teachable Machine.

### Insights
Increasing the variety of examples would sometimes improve the performance of classes. Showing the AI image files was slightly more accurate than showing an image to a camera.

The model would often miscategorize due to the large variety of the samples that often had overlap in style. It would also predictably try to classify some artwork that wasn't apart of certain classes into said classes. Sometimes, the artwork with predominantly faces would trigger the face class and none other. 
I believe it failed because the distinction behind the styles of art between the different eras was too small and too complex for the machine to gleam with so few examples. It's trying its best to look for an example image that best resembles whatever it is presented with and assuming that it must fit into that category. It doesn't appear to be looking for a general trend to the artwork.

The hardest class to train was the Baroque class. This era of art had a lot of overlap with the other classes, so we gave it a bit more data. After we did, there was a noticable improvement in performance for the class.

It was difficult to maintain a good performance once the machine became more complex with more classes. This was mostly because the overlap between the styles made the distinction between each more and more difficult to deduce. 

When we tried adding noise, by using our phones to show images to the machine, it did become a bit more innacurate. It did have similar results as without noise, but you could see that the machine was changing hesitant to put anything at 100% certainty.

It was most suprising, or maybe not that suprising, that the model did best at learning faces. With very few examples, we were able to have it identify not only our faces, but sometimes it saw faces in the art itself. It is both a showcase of the strenght of facial recognition as well as the quality of the artwork, for a face to be seen.

Overall, despite trying our best to choose distinct art styles, it demonstrates how difficult training a machine to detect these varieties actually is. A trained artist, or even untrained, could detect the varieties, but finding the differences with AI showcases a different way of thinking that is needed to achieve this success.
# Text2Image
Text2Image is a new way to classify text. It aims to convert corpus of texts and represent them as Images. Here is a brief explanation of the work. Please refer to ```Text2Image.pdf``` for a more in-depth documentation. The code is a .ipynb in the form .html. It can found as ```Code.html```

<hr>
## How does it work?

Considering the time taken to train NLP models and the amount of data required, an alternative is proposed to visualize texts in the form of images, specifically heatmaps. With reduced training time and the amount of data required, this could be a method to use in cases with very small amount of data/computing power. 

We started out with extracting the TF-IDF values and mapping them according to their position in the piece of text, allowing repetition of words. To reduce the large disparity among the values, all values are plotted on a logarithmic scale. These values were then used to create an 11 x 11 heatmap using seaborn. Adding Gaussian filtering while plotting also seemed to reduce overfitting later on. 

On a dataset of 1000 articles comprising both fake and real news, a resnet34 model was able to achieve an accuracy of ~71% with training time less than 10 minutes.  The result we got seems promising and further study into this may improve the accuracy drastically. Further, immediate areas are visualizing POS taggers combined with TF-IDF values.

Further work is being done to visualize more complex features including n-grams, word embedding like GloVe. Please email to cabhijith001@gmail.com for further work.


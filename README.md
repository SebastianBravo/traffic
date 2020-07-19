# traffic

As a first attempt I tried using a Single convolution layer with 30 filters with a size of 3x3, a single pooling layer with a size of 2x2 and a single hidden layer with 128 units with a dropout of 0.2. The results were not good, the accuracy was little more than 5% and a big loss. I decided to try increasing the number of filters to 60, adding a second hidden layer of 128 units, increasing the first hidden layer units to 326 and increasing dropout to 0.3, this improved the neural network raising the accuaracy a lot, the training however was too slow. In order to achieve a faster trainning, I added a second convolution layer with the same number of filters and a second pooling layer, set both hidden layers units to 128, the trainnig was faster and I got an accuaracy of almost 93%. Finally I reduced the number of units of the second hidden layer to 64 units getting a faster trainning and a final acuaracy of 95% - 96& approximetaly.

### *Some attempts done*:

**Attempt:** 30 3x3 filters, max pooling 2x2, 2 hidden layers 128 units, 0.2 droput  
	loss: 0.9778 - accuracy: 0.5238

**Attempt:** 60 3x3 filters, max pooling 2x2, 1 hidden layer 326 units, 1 hidden layer 128 units, 0.3 droput  
	loss: 0.3162 - accuracy: 0.9345

**Attempt:** 2 layers of 60 3x3 filters and max pooling 2x2, 2 hidden layers 128 units, 0.3 droput  
	loss: 0.2833 - accuracy: 0.9260

**Attempt:** 2 layers of 60 3x3 filters and max pooling 2x2, 1 hidden layer 128 units, 1 hidden layer 64 units, 0.3 dropout  
	loss: 0.1536 - accuracy: 0.9642
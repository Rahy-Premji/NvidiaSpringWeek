# Deep Learning Video Notes


## Video 1: What is a neural network?

- Made up of neurons
- Something that holds a number between 0 and 1
- starts with a network of all the input features
- number example holds the brightness of a grayscale pixel
- output layers are a prediction
- number of hidden layers and neurons in each layer can be changed
- number of layers and neurons determines the structure of the network
- loosely connected to how neural networks work in our brain
- pattern in each layer leads to an output neuron
- pattern recognition fires a specific neuron
- assign a weight to each connection between the neurons
- calculate weighted sum of region we are looking at
- activation needs to be put into a specific range eg 0 to 1
- a sigmoid function does this.
- if we want the weighted sum to be bigger than something then we need to add a bias
- this is done for 1 neuron and needs to be repeated for each neuron and layer
- organise all the activations of one layer into a column
- all the weightings in a matrix
create a matrix vector product
- the sigmoid function is then applied

- sigmoid function squishes weighted sum into a range
- most deep learning uses ReLu
- Rectified linear unit
- if passes a certain threshold then the neuron is acctive, if not then it is not active
- sigmoid was too slow


## Video 2: Gradient Descent, how neural networks learn.

- after training data you show it test data
- therefore testing the database
- initialise bias and weights randomly
- cost function is how bad the prediction is 
- add up the squares of the differences between the actual activations and wanted activations
- costs will be large when it is further away
- average cost is how bad the predction of the model is
- cost function takes weights and biases and outputs the cost of that combination
- trying to find the minimum average cost
- start at random input. shift to left if slope is positive, shift right if slope is negative
- many possibles minimums and current minimum my not be the lowest minimum
- as function gets closer to the minimum the step size reduces to not overshoot the minimum
- compute gradient function
- then step downhill
- Backpropagation is what happens in each weight and piece of data
- learning is just minimising a cost function
- cost function should have a smooth output
- this is why the output has a smooth range ie from 0 to 1
- negative gradient of cost function tell us to nudge up or down
- an adjustment on one weight has a different impact to cost function than another weight
- Random set of input can land on a confident output
- Called Multilayer Perception

## Video 3: What is backpropogration really doing?

- backpropogration is the way to calculate the gradient of the cost function
- senstivity of the weight is the gradient
- desired output nudged up and undersired nudged down
- Increase bias
- increase the weights
- changes the activations from the previous layer
- changing the weights have difference in effects
- higher activation higher effect
- Want other neurons in last layer to become lest active
- adding together all desired effects to happen to second last layer
- this happens for each layer moving backwards
- do this for each training example
- average all those desired changes
- use small batches of training data to increase effeciencey
- stochastic gradient descent
- in order for this to work is lots of training data

## Video 4: Backpropogation calculus

- how sensitive the cost function is to each variable
- cost is equal to the last layer minus the desired outputs whole squared
- how senstive our cost function is to changes in the variables
- uses the chain rule


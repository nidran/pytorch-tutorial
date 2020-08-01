
NN - most common DL algo
DL - many layers to learn from input data
Neurons - active learning units in NN

not a single monolithic system
diff layers share responsibility

lower layers - extract granular info 
higher layers - abstraction into higher features 

L0 - pixel
L1 : edge
L2: Object
L3 : feature 

Visible layer - input layer, output layer
Hidden layers - extracting granular data, patterns,
Feed forward NN - input is output of previous layer


Each layer - interconnetced neurons
Allows for hierachical learning or feature learning


Operation of single neuron - Mathematical function
input to neuron - X variables or features (vector )
applies funtion
produces scalar Y

For an active /learning neuron a change in inputs should trigger change in outputs

Sclaar Y - fed into neuron of next layer
single neuron can be connected to any no of neurons
every interconnection has a weight - how impt is the interconnection of the first neuron from the ouptut layer to the input in the next layer
(or) - how sensitive is the output of the first neuron for the second neuron
- high sensitive - connection strong - weight increases 
- neurons that fre together are wired together
- Model params (W) - all the weights associated with all interconnection define ur model
- internconnection bw neurons is data - edges in computational graph  - tensors - multidimensional data
- NN works on these Model params.
- Once model is trained , wt is assigned to all interconnections
- Each neuron applies 2 functions to its inputs 
	- Affine transformation - linear - only leanrs linears functions btw input and output
	- Wx+ b
	- wt sum with bias added
	- Activation function - non linear relationships
	- when activation function passes the output of affine transformation as it is - linear neuron - Identity function
- Common Activation fn
	- ReLU ( Rectivied linear unit )- Max of (input, 0)
	- logit 
	- tanh - sigmoid fn
	- step 
	- softmax - sigmoid/ logit curve - multi class classification
	- each has gradient 
		- active regions - sensitive to data
			- to adjust weights the activation functions should operate in active region
		- saturated region - not sensitive
- actual wts & b are determined during training, its random in beginning
	
Pytorch - dl frmwk
tensors - multidimesnion array - can perform parallel computations
Tape based autograd
NN can be redefined dynamically - diff frm TF, CNTK
computation graph - dynamic

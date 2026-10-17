- What are the 3 areas of NLP?
    - Translate
    - NER
    - Sentiment


- What is NER?
    - NER (Named Entity Recognition) is a subtask of NLP that involves `identifying and classifying` named entities in text into predefined categories such as `person names, organizations, locations, dates,` and more. 
    - It `helps in extracting structured information from unstructured text data`, enabling `applications` like `information retrieval, question answering, and knowledge graph construction`
    
- What are  n-gram models(1990)? # Statistical Language Models
    - N-gram models are a type of probabilistic language model that predicts the next word in a sequence based on the previous n-1 words. 
    - They are based on the assumption that the probability of a word depends only on the previous n-1 words, which is known as the Markov assumption. 
    - N-gram models are commonly used in NLP tasks such as `speech recognition, machine translation, and text generation`.
    - the term n-gram refers to a contiguous sequence of n items (words or characters) in a given text. For example, in the sentence "I love natural language processing," the 2-grams (bigrams) would be "I love," "love natural," "natural language," and "language processing."

- Neural_LM's
    - Word2vec (2013)
        - Word2vec is a neural network-based model that learns to represent words as dense vectors in a continuous vector space. It uses a shallow neural network architecture to predict the context words given a target word (or vice versa) and captures semantic relationships between words based on their co-occurrence patterns in large text corpora. Word2vec has been widely used for various NLP tasks, `including word similarity, analogy reasoning, and as input features for downstream models`.
    - context modelling
        - Context modeling in NLP refers to the process of capturing and utilizing the surrounding context of words or phrases in a text to improve understanding and prediction. It involves considering the relationships between words and their neighboring words to better represent their meaning and usage. Context modeling is essential for tasks such as `language modeling, machine translation, sentiment analysis, and named entity recognition`, as it allows models to disambiguate word meanings, capture dependencies, and generate more accurate predictions based on the context in which words appear.

- Transformers (2017)
    - Transformers are a type of neural network architecture that was introduced in the paper "Attention is All You Need" by Vaswani et al. in 2017. They are designed to handle sequential data, such as text, and have become the foundation for many state-of-the-art NLP models.
    - The key innovation of transformers is the self-attention mechanism, which allows the model to weigh the importance of different words in a sequence when making predictions. This enables transformers to capture long-range dependencies and relationships between words more effectively than previous architectures like RNNs and LSTMs.
    - Transformers have been widely adopted in NLP tasks such as `machine translation, text summarization, question answering, and language modeling`, and have led to the development of powerful pre-trained models like BERT, GPT, and T5.


- what is pretraining?
    - Pretraining is a process in machine learning, particularly in natural language processing (NLP), where a model is trained on a large dataset to learn general patterns and representations before being fine-tuned on a specific task. The goal of pretraining is to enable the model to acquire a broad understanding of language, which can then be leveraged for various downstream tasks.
    - In the context of NLP, pretraining often involves training a model on a large corpus of text using unsupervised or self-supervised learning techniques, such as predicting missing words (masked language modeling) or predicting the next word in a sequence (causal language modeling). This allows the model to learn semantic and syntactic relationships between words, phrases, and sentences.

- What are the 4 main architectures of DL?
    - FFNN (Feedforward Neural Networks)
    - MLP (Multilayer Perceptron)
        - input layer
        - hidden layer
        - output layer
    - CNN (Convolutional Neural Networks)
        - we did weight sharing and pooling
        - what is weight sharing?
            - Weight sharing is a technique used in convolutional neural networks (CNNs) where the same set of weights (filters or kernels) is applied across different spatial locations of the input data. 
            - This means that the same filter is used to detect features in different parts of the input, allowing the network to learn spatial hierarchies and patterns more efficiently.
            - The main benefits of weight sharing include:
                1. Reduced number of parameters: By using the same weights across different locations, the total number of parameters in the network is significantly reduced, which helps prevent overfitting and makes the model more computationally efficient.
                2. Translation invariance: Weight sharing allows the network to recognize features regardless of their position in the input, making it more robust to translations and variations in the input data.
                3. Improved generalization: With fewer parameters to learn, the model can generalize better to unseen data, leading to improved performance on tasks such as image classification and object detection.
    - RNN (Recurrent Neural Networks)

- Explain the backpropagation algorithm
    - Backpropagation is a supervised learning algorithm used for training artificial neural networks. It is a method for updating the weights of the network based on the error between the predicted output and the actual target output. 
    - The goal of backpropagation is to minimize the loss function, which measures the difference between the predicted and actual outputs.
    - The backpropagation algorithm consists of two main steps: forward pass and backward pass. 
        - In the forward pass, the input data is passed through the network, and the output is computed. 
        - In the backward pass, the error is propagated backward through the network, and the weights are updated using gradient descent or other optimization algorithms. 
        - This process is repeated iteratively until the network converges to an optimal set of weights that minimize the loss function.

- what is self-attention?
    - Self-attention is a mechanism used in neural networks, particularly in transformer architectures, that allows the model to weigh the importance of different elements in a sequence when processing a specific element. 
    - In self-attention, each element in the input sequence is compared to every other element to compute attention scores, which indicate how much focus should be given to each element when generating the output for a specific element. 
    - This enables the model to capture long-range dependencies and relationships between elements in the sequence, making it particularly effective for tasks involving sequential data, such as natural language processing and time series analysis.

- What is WK,WQ,WV in transformers?
    - In transformers, WK, WQ, and WV refer to the weight matrices used in the self-attention mechanism. 
        - WQ (Weight for Query): This matrix is used to transform the input embeddings into query vectors. The query vectors are used to compute attention scores that determine how much focus should be given to each input token when processing a specific token.
        - WK (Weight for Key): This matrix is used to transform the input embeddings into key vectors. The key vectors are compared with the query vectors to calculate attention scores, which indicate the relevance of each input token to the current token being processed.
        - WV (Weight for Value): This matrix is used to transform the input embeddings into value vectors. The value vectors are combined based on the attention scores to produce the final output of the self-attention mechanism.
    - These weight matrices are learned during training and play a crucial role in enabling transformers to capture relationships between tokens in a sequence effectively.

- What is a Vanishing gradient problem?
    - The vanishing gradient problem is a challenge that arises during the training of deep neural networks, particularly in architectures like recurrent neural networks (RNNs) and deep feedforward networks. It occurs when the gradients of the loss function with respect to the model's parameters become very small as they are propagated backward through the layers of the network during backpropagation.
    - As a result, the weights of the earlier layers receive very small updates, making it difficult for the network to learn and converge effectively. This can lead to slow training, poor performance, and difficulty in capturing long-range dependencies in sequential data.
    - The vanishing gradient problem is often addressed using techniques such as:
        1. Using activation functions that mitigate the issue (e.g., ReLU instead of sigmoid or tanh).
        2. Implementing architectures like LSTMs or GRUs that are designed to handle long-term dependencies more effectively.
        3. Applying gradient clipping to prevent gradients from becoming too small or too large during training.


- RNN and LSTMs 
    - RNN (Recurrent Neural Networks) are a type of neural network architecture designed to handle sequential data. They have a feedback loop that allows information to persist across time steps, enabling them to capture temporal dependencies in the input data. RNNs are commonly used for tasks such as language modeling, speech recognition, and time series prediction.
    - LSTMs (Long Short-Term Memory networks) are a specific type of RNN that addresses the vanishing gradient problem, which can occur in standard RNNs when learning long-term dependencies. LSTMs introduce memory cells and gating mechanisms (input, output, and forget gates) that allow them to selectively retain or discard information over time. This makes LSTMs more effective at capturing long-range dependencies in sequential data compared to traditional RNNs.

- in transformers the tranings can be parallelized , whereas in RNNs the training is sequential and cannot be parallelized, because RNNs process one time step at a time, and the output of one time step is dependent on the previous time step. This sequential nature of RNNs makes it difficult to parallelize the training process, as each time step must be computed in order. In contrast, transformers use self-attention mechanisms that allow them to process all input tokens simultaneously, enabling parallelization and faster training times.

- We have learnt 4 architectures
    - MLP : this is compose of linear layers, and is used for simple tasks like classification and regression.
        - The model is composed of linear layers and non-linear activations (assuming Relu is used). Therefore, the code contains only nn.linear and torch.relu
        ```python
        class MLP (nn.Module) :

            def __init__(self, x_dim, h1_dim, h2_dim, out_dim):
                super().__init__()
                self.w1 = nn.Linear(x_dim, h1_dim, bias=True)
                self.w2 = nn.Linear(h1_dim, h2_dim, bias=True)
                self.w3 = nn.Linear(h2_dim, out_dim, bias=True)

            def forward(self, x):
                out = torch.relu(self.w1(x))
                out = torch.relu(self.w2(out))
                out = torch.relu(self.w3(out))
                return out
        ```
    - CNN : this is used for image processing, and is composed of convolutional layers, pooling layers, and fully connected layers. The convolutional layers are used to extract features from the input image, while the pooling layers are used to reduce the spatial dimensions of the feature maps. The fully connected layers are used to make predictions based on the extracted features.
        - The model is composed of convolutional layers, pooling layers, and fully connected layers. Therefore, the code contains nn.Conv2d, nn.MaxPool2d, and nn.Linear
        - The model is composed of nn.linear,nn.Conv2d,MaxPool2D and torch.relu
        ```python



        class CNN (nn. Module) :
            def __init__(self):
                super(CNN, self).__init__()
                self.conv1 = nn.Conv2d(3, 6, 5) # 5 is the filter size, 3 is the number of input channels, 6 is the number of output channels | 5x5 filter size, 3 input channels (RGB), 6 output channels (feature maps)
                self.pool = nn.MaxPool2d(2, 2)
                self.conv2 = nn.Conv2d(6, 16, 5)# 6 comes from the output of the previous layer, 16 is the number of output channels | 5x5 filter size, 6 input channels (from previous layer), 16 output channels (feature maps)
                self.fc1 = nn.Linear(16 * 5 * 5, 10) # 16 comes from the output of the previous layer, 5x5 is the size of the feature map, 10 is the number of output classes (flattening the feature map to a vector of size 10)
                self.fc2 = nn.Linear(10, 4) # 10 comes from the output of the previous layer, 4 is the number of output classes
                self.fc3 = nn.Linear(4, 2) # 4 comes from the output of the previous layer, 2 is the number of output classes

            def forward(self, x) :
                x = self.pool(F.relu(self.conv1(x)))
                X = self.pool(F.relu(self.conv2(x)))
                x = x.view(-1, 16 * 5 * 5)
                x = F.relu(self.fc1(x))
                x= F.relu(self.fc2(x))
                x = self.fc3(x)
                return x
        ```

    - RNN : this is used for sequential data, and is composed of recurrent layers and fully connected layers. The recurrent layers are used to capture temporal dependencies in the input data, while the fully connected layers are used to make predictions based on the extracted features.
        - The model is composed of nn.RNN and nn.Linear
        ```python
        class RNN(torch.nn.Module) :
            def __init__(self, vocab_size, embed_dim, hidden_dim, num_class) :
                super().__init__()
                self.embedding = nn.Embedding(vocab_size,
                embed_dim,  
                padding_idx=0)
                self.rnn = nn.RNN(embed_dim,
                hidden_dim,
                batch_first=True)
                self.fc = nn.Linear(hidden_dim, num_class)

            def forward(self, x, length)
                x = self.embedding(x)
                x = pack_padded_sequence (x,
                                    lengths=length,
                enforce_sorted=False,
                batch_first=True)

                x = self. rnn (x)
                X = self.fc(x[-1])
                return x
        ``` 
    - Transformer : this is used for sequential data, and is composed of self-attention layers and fully connected layers. The self-attention layers are used to capture long-range dependencies in the input data, while the fully connected layers are used to make predictions based on the extracted features.
        - The model is composed of nn.MultiheadAttention and nn.Linear
        ```python
        class TRANSFORMER(torch.nn.Module) :
            def __init__(self, vocab_size, embed_dim, hidden_dim, num_class) :
                super().__init__()
                self.embedding = nn.Embedding (vocab_size,
                embed_dim,
                padding_idx=0)
                self.transformer = nn.Tranaformer (dmodel,
                nhead,
                num_encoder_layers,
                num_decoder_layers,
                dim_feedforward)
                self.fc = Linear (dmodel, vocab_size)

            def forward(self, x, length)
                x = self.embedding (x)
                x = self.tranaformor (x)
                x = self.fc(x[1])
                return x
        ```

- What is a convolutional layer?
    - A convolutional layer is a fundamental building block of convolutional neural networks (CNNs) that is designed `to process and extract features from input data`, such as images or sequences. It applies a set of learnable filters (also called kernels) to the input data through a mathematical operation called convolution.
    - The convolution operation involves sliding the filters over the input data and computing the dot product between the filter weights and the corresponding input values. This results in a feature map that highlights specific patterns or features present in the input data, such as edges, textures, or shapes.
    - Convolutional layers are typically followed by activation functions (e.g., ReLU) and pooling layers to introduce non-linearity and reduce the spatial dimensions of the feature maps, respectively. By stacking multiple convolutional layers, CNNs can learn hierarchical representations of the input data, enabling them to perform tasks such as image classification, object detection, and segmentation effectively.

- What is a pooling layer?
    - A pooling layer is a component of convolutional neural networks (CNNs) that is `used to reduce the spatial dimensions of the feature maps generated by convolutional layers`. It performs a downsampling operation, which helps to decrease the number of parameters and computations in the network, as well as to make the model more robust to variations in the input data.
    - The most common types of pooling operations are max pooling and average pooling:
        - Max pooling: This operation selects the maximum value from a defined region (e.g., a 2x2 window) of the feature map. It retains the most prominent features while discarding less important information.
        - Average pooling: This operation computes the average value of a defined region of the feature map, providing a smoother representation of the features.
    - Pooling layers help to achieve `translation invariance, meaning that small translations or shifts in the input data will not significantly affect the output of the network`. By reducing the spatial dimensions, pooling layers also `help to prevent overfitting and improve generalization performance on unseen data`.
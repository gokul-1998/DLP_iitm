- what is peft?
    - PEFT stands for Parameter-Efficient Fine-Tuning.
    -  It is a technique used in machine learning, particularly in the context of large language models, to `fine-tune a pre-trained model on a specific task or dataset while only updating a small subset of the model's parameters`. 
    - This approach allows for efficient adaptation of the model to new tasks without the need for extensive computational resources or large amounts of labeled data.

- bitsandbytes
    - BitsAndBytes is a library that provides efficient implementations of various machine learning algorithms and techniques, particularly for training large models. 
    - It includes support for `mixed precision training, quantization`, and other optimizations that can help reduce memory usage and improve training speed.

- what is pre-training?
    - Pre-training is a technique in machine learning where a model is `first trained on a large dataset to learn general features and representations before being fine-tuned on a smaller, task-specific dataset`. 
    - This approach allows the model to leverage the knowledge gained during pre-training to improve performance on the target task.

- what is instruction tuning?
    - Instruction tuning is a technique used in natural language processing (NLP) to `fine-tune a pre-trained language model on a specific task or dataset by providing it with task-specific instructions or prompts`. 
    - This approach allows the model to better understand the requirements of the task and generate more accurate and relevant outputs.

- what is positional embedding?
    - Positional embedding is a technique used in transformer models to `encode the position of tokens in a sequence`. 
    - Since transformers do not have a built-in notion of order, positional embeddings are added to the input embeddings to provide information about the relative or absolute position of tokens in the sequence. 
    - This allows the model to capture the sequential nature of the data and improve its performance on tasks such as language modeling and machine translation.
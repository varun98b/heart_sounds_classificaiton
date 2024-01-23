# heart_sounds_classificaiton

The dataset provided is about Heart sounds generated by the beating heart, In our code we are trying to analyse the audio files and classify them using LSTM, Vanilla RNN and GRU and deciding the best model while exploring the hyperparameters.

Dataset: http://www.peterjbentley.com/heartchallenge/

### Data Preprocessing:

•	Define data generators for the training, validation, and possibly test sets specific to audio data.

•	Utilize techniques like Mel-frequency cepstral coefficients (MFCCs) extraction or other spectral features to convert raw audio data into a form suitable for training with recurrent networks.

### Model Architecture:

•	LSTM Model: Define an architecture using LSTM layers suitable for heart sound classification. Given the sequential nature of audio data, LSTM can capture long-term dependencies in the data.

•	Vanilla RNN Model: Implement a model using SimpleRNN layers, which are the most basic form of recurrent units. This will serve as a baseline to compare against more complex models.

•	GRU Model: Design a model using GRU layers, which offer a balance between the complexity of LSTM and the simplicity of Vanilla RNN.

•	For all architectures, consider integrating the activations and Dropout layers to prevent overfitting.

•	The models used, like lstm_model, rnn_model, and gru_model.

•	Additionally, grid search is used for different hyperparameters to find the best accuracy parameters.

### Compilation:

•	Compile each model using an optimizer like Adamax, RMSprop. Given that it's a classification problem, use 'categorical_crossentropy' as there are three classes.

•	Track metrics like accuracy, mean square error and mean absolute error to monitor the model's performance during training.

### Training:

•	Train each model—LSTM, Vanilla RNN, and GRU—using the training and validation data generators.

•	Utilize callbacks like EarlyStopping and ModelCheckpoint to halt training when validation performance plateaus and save the best model respectively.

•	Visualize the training and validation loss and accuracy over epochs to inspect convergence and potential overfitting.

### Evaluation and Model Comparison:

•	Evaluate each model on a separate test set using the evaluate method.

•	Compare the performance of the LSTM, Vanilla RNN, and GRU models to determine the best architecture for the task.

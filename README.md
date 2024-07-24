# Speech_KWS_Lightweight
**Objective:** Building a lightweight model (CNN or DNN) that maintains a high degree of accuracy in classifying speech keyword audio samples. 

**Key Idea:** Try to limit the number of parameters and multiplies of the model, making it as lightweight as possible, while maintaining close to 90% categorical accuracy. For this, I utilize varying strides and pooling sizes, adding image enhancing techniques (like Gaussian and Sobel convolutions) and addition of a Non-Linear LoRA Layer. 

**Dataset:** The Google Speech Commands Dataset is chosen so as to cover a wide array of speech sounds as trainable data. The model is trained on a subset of 8 classes (chosen to span the range of speech sounds), with 3000 audio samples each. The data is preprocessed and optimized over various parameters like input type (MFCC vs Spectrogram), number of features (stacking and adding delta features to MFCC) and adding Gaussian white noise. 

For the results, please visit my Portfolio site: https://jelinr.github.io/

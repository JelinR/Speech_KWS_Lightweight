# Speech_KWS_Lightweight
**Objective:** Building a lightweight model (CNN or DNN) that maintains a high degree of accuracy in classifying speech keyword audio samples. 

**Key Idea:** Try to limit the number of parameters and multiplies of the model, making it as lightweight as possible, while maintaining close to 90% categorical accuracy. For this, I utilize varying strides and pooling sizes, adding image enhancing techniques (like Gaussian and Sobel convolutions) and addition of a Non-Linear LoRA Layer. 

**Dataset:** The Google Speech Commands Dataset is chosen so as to cover a wide array of speech sounds as trainable data. The model is trained on a subset of 8 classes (chosen to span the range of speech sounds), with 3000 audio samples each. The data is preprocessed and optimized over various parameters like input type (MFCC vs Spectrogram), number of features (stacking and adding delta features to MFCC) and adding Gaussian white noise. 

**Result:** The best performing model, cnn_spect_64 (32k parameters), is able to provide 87%-89% categorical accuracy on two different test sets (different 8 classes chosen) of the Google Speech Commands Dataset. With an inference time of 37 ms and a memory load of 90 KB, this is a very lightweight architecture that maintains a high classification accuracy. This competes against standard SoTA models like TDNN, which contains 251k parameters and achieves 94% accuracy. Additionally, compared to the standard wake word inference time of 10-50 ms, this model performs very satisfactory in this regards too. 

For more information, please visit my Portfolio site: https://jelinr.github.io/

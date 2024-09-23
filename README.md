# Speech_KWS_Lightweight
**Objective:**  To build a lightweight model (limiting parameters and multiplies) that maintains a high degree of accuracy in classifying speech keyword audio samples. 

**Key Idea:**  Try to limit the number of parameters and multiplies of the model, making it as lightweight as possible, while maintaining decent categorical accuracy. For this, I utilize varying strides and pooling sizes, adding image enhancing techniques (like Gaussian and Sobel convolutions) and addition of Non-Linear LoRA Layer and Channel Attention Blocks (CAB). 

**Dataset:** Google Speech Commands Dataset is chosen so as to cover a wide array of speech sounds as trainable data. The model is trained on a subset of 8 classes (chosen to span the range of speech sounds), with 3000 audio samples each. Additionally, the model is tested on the standard V12 dataset, a 12-keyword subset of the same dataset, which enables fair comparison with other performing models. 

**Result:** The best performing model, cnn_spect_cab (31k parameters), provides 92.5% accuracy on the 8-keyword dataset and 90.25% accuracy on the V12 dataset. With an inference time of 39 ms and a memory load of 90 KB, this is a very lightweight architecture that maintains a high classification accuracy (>90%). Additionally, in comparison with SoTA models, taking into account both accuracy and number of parameters, this model is seen to be much more efficient.

For more information, please visit my Portfolio site: https://jelinr.github.io/

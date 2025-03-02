# **Sentiment Analysis**

Sentiment analysis model to classify movie reviews as **positive** or **negative**. The model is implemented using **TensorFlow and Keras**, with **word frequency vectors** as input.  

---

### **1. Data Preprocessing**
- **Loading Data**:  
  - Reviews are loaded from `reviews.txt`  
  - Labels (positive/negative) are loaded from `labels.txt`  

- **Text Cleaning & Tokenization**:  
  - Convert text to lowercase.  
  - Remove punctuation and non-alphabetic characters.  
  - Split text into words.  

- **Building Vocabulary**:  
  - Count word occurrences.  
  - Keep the **10,000 most frequent words**.  

- **Word-to-Index Mapping `word2idx`**:  
  - Each word is assigned a unique index.  
 

- **Vectorizing Reviews**:  
  - Convert each review into a **word frequency vector** of length **10,000**.  


---

### **2. Splitting Data**
- **Train/Test Split** (90% train, 10% test).  
- **Stratified sampling** ensures an equal distribution of positive/negative reviews.  

---

### **3. Building the Neural Network**
The model is a **feedforward neural network** with:
- **Input Layer**: 10,000 features.  
- **Hidden Layers**:
  - **Dense(256, ReLU) + Dropout(0.5)**
  - **Dense(128, ReLU, L2 regularization) + Dropout(0.3)**
  - **Dense(64, ReLU)**  
- **Output Layer**: Softmax activation.  


---

### **4. Training the Model**
- **Optimizer**: Adam `learning_rate=0.001`  
- **Evaluation Metrics**: Accuracy, Precision, Recall  
- **Early Stopping**

---

### **5. Evaluating the Model**
- The model is evaluated on the **test set**.  
- Metrics reported:
  - **Accuracy**
  - **Precision**
  - **Recall**


---

### **6. Making Predictions**
The model can classify new sentences as **positive or negative**.  

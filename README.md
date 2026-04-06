 ICAGnet: Incorporating Attention with Deep Learning Approach for Audio Image Descriptions

📌 Overview

**ICAGnet** is an AI-powered assistive system designed to help visually impaired individuals understand their surroundings. The model takes an image as input, generates a natural language description, and converts it into speech.

This project combines **Computer Vision**, **Natural Language Processing**, and **Text-to-Speech (TTS)** to create a complete multimodal pipeline.

---

## 🚀 Features

* 🖼️ Image Captioning using deep learning
* 🧠 Encoder-Decoder architecture (CNN + LSTM)
* 🔊 Text-to-Speech output using gTTS
* 📊 Trained on real-world image-caption datasets
* ♿ Assistive application for visually impaired users

---

## 🏗️ Architecture

The model follows a classic **Encoder-Decoder framework**:

```
Image → CNN Encoder → Feature Vector → LSTM Decoder → Caption → Text-to-Speech
```

### 🔹 Encoder (CNN)

* Extracts high-level features from input images
* Typically uses pretrained models like **ResNet / InceptionV3**

### 🔹 Decoder (LSTM)

* Generates captions word-by-word
* Takes image features + previous words as input

### 🔹 Text-to-Speech

* Converts generated caption into audio using **gTTS**

---

## 🧠 How It Works

1. **Image Input**
   The system takes an image as input.

2. **Feature Extraction**
   A pretrained CNN encodes the image into a feature vector.

3. **Caption Generation**
   An LSTM-based decoder generates a caption sequentially:

   ```
   <start> → a → man → walking → <end>
   ```

4. **Speech Output**
   The generated caption is converted into audio for accessibility.

---

## 📂 Dataset

* Image-caption dataset (e.g., Flickr8k / Flickr30k / custom dataset)
* Each image has multiple human-written captions

Example:

```
image1.jpg → "A man walking on the street"
```

---

## ⚙️ Training Process

* Tokenization of captions
* Vocabulary creation
* Sequence padding
* Teacher forcing during training
* Loss: Categorical Crossentropy

---

## 📈 Evaluation

* Qualitative: Visual inspection of generated captions
* Quantitative (optional): BLEU score

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* OpenCV / PIL
* NumPy, Pandas
* gTTS (Google Text-to-Speech)

---

## ▶️ Usage

1. Clone the repository:

```bash
git clone https://github.com/yourusername/eye-for-the-blind.git
cd eye-for-the-blind
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook/script:

```bash
jupyter notebook
```

4. Provide an image → get caption + audio output

---

## 📌 Example Output

**Input Image:**
*A man riding a bicycle*

**Generated Caption:**
"A man riding a bicycle on the road"

**Audio Output:**
🔊 Plays generated description

---

## 🔮 Future Improvements

* Add **Attention Mechanism** for better caption quality
* Replace LSTM with **Transformer-based decoder**
* Deploy as a **mobile/web application**
* Real-time camera integration

---

## 🤝 Contributing

Contributions are welcome! Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is open-source and available under the MIT License.

---

## 🙌 Acknowledgements

* Image Captioning research papers
* Open datasets like Flickr
* Google Text-to-Speech (gTTS)

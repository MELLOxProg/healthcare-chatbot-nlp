# 🧑‍⚕️ Healthcare Chatbot with NLP

<div align="center">

![Python](https://img.shields.io/badge/python-v3.11+-blue.svg)
![Flask](https://img.shields.io/badge/flask-v3.1.0+-green.svg)
![Transformers](https://img.shields.io/badge/transformers-v4.51.0+-orange.svg)
*An intelligent healthcare chatbot powered by Hugging Face Transformers for domain-specific customer support*

[Installation](#installation) • [Usage](#usage) • [Model](#model) • [Testing](#testing) • [Contributing](#contributing)

</div>

---

## 📋 Overview

**Dr. Assist** is a sophisticated healthcare chatbot built using state-of-the-art Natural Language Processing (NLP) techniques. The chatbot leverages a fine-tuned T5 model from Hugging Face Transformers to provide accurate, domain-specific responses for healthcare customer support queries.

### ✨ Key Features

- 🤖 **Fine-tuned T5 Model**: Custom-trained on healthcare domain data
- 🌐 **Web Interface**: Clean, responsive UI with chat functionality
- 🚀 **Flask API**: RESTful backend for easy integration
- 📊 **Domain-Specific**: Specialized for healthcare queries and support
- 🔄 **Real-time Chat**: Interactive chat interface with immediate responses
- 📱 **Responsive Design**: Works seamlessly across devices

---

## 🖼️ Demo

### Web Interface Preview

![Healthcare Chatbot Interface](ss.png)

The Dr. Assist chatbot features a modern, responsive web interface with:
- Clean design with healthcare branding
- Floating chat button for easy access
- Interactive chat window with real-time responses
- Professional styling using Tailwind CSS

### How to Use the Interface

1. **Launch the application** by running `python main.py`
2. **Open your browser** to `http://localhost:5000`
3. **Click the chat button** (💬) located in the bottom-right corner
4. **Type your healthcare questions** in the chat input field
5. **Receive instant responses** from the AI-powered Dr. Assist

---

## 🚀 Quick Start

### Prerequisites

- Python 3.11+
- Git with Git LFS support
- 4GB+ RAM (recommended for model loading)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/MELLOxProg/healthcare-chatbot-nlp.git
   cd healthcare-chatbot-nlp
   ```

2. **Create and activate virtual environment**
   ```bash
   python -m venv chatbot_env
   # On Windows
   chatbot_env\\Scripts\\activate
   # On macOS/Linux
   source chatbot_env/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python main.py
   ```

5. **Access the chatbot**
   Open your browser and navigate to `http://localhost:5000`

---

## 💻 Usage

### How to Interact with the Chatbot

1. **Start the Flask server**
   ```bash
   python main.py
   ```

2. **Open your browser** to `http://localhost:5000`

3. **Click the chat button** (💬) located in the **bottom-right corner** of the web page

4. **Type your message** in the chat input field that appears

5. **Click "Send"** or press Enter to get a response from Dr. Assist

### Example Interaction

Here's how a typical conversation looks:

**You**: "What are the symptoms of the flu?"

**🧑‍⚕️ Dr. Assist**: "Common flu symptoms include fever, chills, muscle aches, cough, congestion, runny nose, headaches, and fatigue. If you're experiencing these symptoms, consider contacting your healthcare provider."

### Communication Method

The chatbot is designed for **web-based interaction only**. Users communicate through:
- The floating chat interface accessible via the chat button
- Real-time message exchange within the chat window
- No direct API calls needed for end users

---

## 🧪 Testing

### Sample Questions for Testing

![Sample Questions](questions.png)

The project includes a comprehensive set of test questions in `Questions.md` to help you evaluate the chatbot's performance. These questions are carefully curated to test various aspects of the healthcare domain knowledge.

#### Question Categories

**Common Healthcare Queries:**
- Symptom identification ("What are the symptoms of the flu?")
- Medical procedures ("How can I schedule an appointment with my doctor?")
- Medication management ("I forgot to take my medication. What now?")
- Health monitoring ("How do I know if I have a fever?")

**Edge Cases for Robustness Testing:**
- Medication safety scenarios
- Dosage-related questions
- Account management queries

#### Using the Test Questions

1. **Navigate to** `Questions.md` in the project root
2. **Copy any question** from the provided list
3. **Paste it** into the chat interface
4. **Evaluate the response** quality and accuracy
5. **Test edge cases** to ensure robust performance

These test questions help ensure the chatbot provides accurate, helpful responses across various healthcare scenarios while maintaining appropriate boundaries for medical advice.

---

## 🧑‍⚕️ Model Architecture

### Model Details

- **Base Model**: T5 (Text-to-Text Transfer Transformer)
- **Model Size**: ~242MB
- **Training Data**: Healthcare-specific customer support conversations
- **Fine-tuning**: Domain-adapted for healthcare queries
- **Tokenizer**: SentencePiece-based T5 tokenizer

### Model Components

```
chatbot_model/
├── model.safetensors      # Main model weights (242MB)
├── config.json           # Model configuration
├── tokenizer_config.json # Tokenizer settings
├── special_tokens_map.json
├── added_tokens.json
├── generation_config.json
└── spiece.model          # SentencePiece model
```

### Performance

- **Max Input Length**: 250 tokens
- **Max Output Length**: 250 tokens
- **Beam Search**: 4 beams for better generation quality
- **Early Stopping**: Enabled for efficient generation

---

## 📁 Project Structure

```
healthcare-chatbot-nlp/
├── 📁 chatbot_model/           # Trained T5 model files
│   ├── model.safetensors       # Model weights (Git LFS)
│   ├── config.json            # Model configuration
│   └── ...                    # Other model files
├── 📁 templates/              # HTML templates
│   └── index.html             # Main web interface
├── 📁 results/                # Training results and checkpoints
├── 📄 main.py                 # Flask application
├── 📄 domain_specific_chatbot_data.csv  # Training dataset
├── 📄 Building_HealthCare_Chatbot_*.ipynb  # Training notebook
├── 📄 Questions.md            # Sample questions for testing
├── 📄 requirements.txt        # Python dependencies
└── 📄 README.md              # This file
```

---

## 🛠️ Development

### Training Your Own Model

The project includes a comprehensive Jupyter notebook that demonstrates the entire training process:

**`Building_HealthCare_Chatbot_for_Domain_Specific_Customer_Support_With_Huggingface_transformers_machine_learning.ipynb`**

This notebook covers:
- Data preprocessing and cleaning
- Model fine-tuning with Hugging Face Transformers
- Training configuration and hyperparameters
- Model evaluation and validation
- Saving the trained model

### Key Technologies

| Technology | Purpose | Version |
|------------|---------|---------|
| **Python** | Core language | 3.11+ |
| **Flask** | Web framework | 3.1.0+ |
| **Transformers** | Model library | 4.51.0+ |
| **PyTorch** | Deep learning framework | 2.6.0+ |
| **SentencePiece** | Tokenization | 0.2.0+ |
| **Git LFS** | Large file storage | - |

### Environment Setup

The project uses a virtual environment to manage dependencies:

```bash
# Create virtual environment
python -m venv chatbot_env

# Activate (Windows)
chatbot_env\\Scripts\\activate

# Activate (macOS/Linux)
source chatbot_env/bin/activate

# Install dependencies
pip install -r requirements.txt
```

---

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### Getting Started

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/amazing-feature
   ```
3. **Make your changes**
4. **Test thoroughly**
5. **Commit your changes**
   ```bash
   git commit -m "Add amazing feature"
   ```
6. **Push to your branch**
   ```bash
   git push origin feature/amazing-feature
   ```
7. **Open a Pull Request**

### Development Guidelines

- Follow PEP 8 style guidelines
- Add docstrings to functions and classes
- Include tests for new features
- Update documentation as needed
- Ensure model files are handled with Git LFS

---

## 📊 Performance & Metrics

### Model Performance

The healthcare chatbot has been trained and evaluated on domain-specific data:

- **Training Dataset**: Healthcare customer support conversations
- **Model Architecture**: T5-based conditional generation
- **Optimization**: Fine-tuned for healthcare domain terminology
- **Response Quality**: Contextually aware and medically informed

### System Requirements

| Component | Minimum | Recommended |
|-----------|---------|-------------|
| **RAM** | 4GB | 8GB+ |
| **Storage** | 1GB | 2GB+ |
| **Python** | 3.11 | 3.11+ |
| **GPU** | Optional | CUDA-compatible |

---

## 🔧 Configuration

### Model Configuration

The model can be configured through the generation parameters in `main.py`:

```python
outputs = model.generate(
    inputs["input_ids"],
    max_length=250,        # Maximum response length
    num_beams=4,          # Beam search width
    early_stopping=True   # Stop when EOS token is generated
)
```

### Flask Configuration

Modify the Flask app settings for production:

```python
if __name__ == "__main__":
    app.run(
        debug=False,      # Set to False for production
        host='0.0.0.0',   # Allow external connections
        port=5000         # Default port
    )
```

---

## 🐛 Troubleshooting

### Common Issues

**Issue**: Model loading takes too long
- **Solution**: Ensure you have sufficient RAM (4GB+)
- **Alternative**: Use a smaller model variant

**Issue**: CUDA out of memory
- **Solution**: Reduce batch size or use CPU inference
- **Code**: Modify device configuration in `main.py`

**Issue**: Git LFS files not downloading
- **Solution**: Ensure Git LFS is installed and initialized
```bash
git lfs install
git lfs pull
```

### Debug Mode

Enable detailed logging by setting Flask debug mode:

```python
app.run(debug=True)
```

---

## 🙏 Acknowledgments

- **Hugging Face** for the Transformers library and T5 model
- **Flask** team for the lightweight web framework
- **PyTorch** community for the deep learning framework
- **Healthcare domain experts** for data insights and validation

---

## 📞 Support

For questions, issues, or contributions:

- **Create an issue** on GitHub
- **Star the repository** if you find it helpful
- **Fork and contribute** to make it even better

---

<div align="center">

**Built with ❤️ for better healthcare customer support**

[⭐ Star this repository](https://github.com/MELLOxProg/healthcare-chatbot-nlp) • [🐛 Report Bug](https://github.com/MELLOxProg/healthcare-chatbot-nlp/issues) • [💡 Request Feature](https://github.com/MELLOxProg/healthcare-chatbot-nlp/issues)

</div>

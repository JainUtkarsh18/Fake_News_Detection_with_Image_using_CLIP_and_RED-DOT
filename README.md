# Fake_News_Detection_with_Image_using_CLIP_and_RED-DOT Classifier
## Table of Contents

- [Overview](#overview)
- [Part 1: Inference Script](#part-1-inference-script)
- [Part 2: Local Deployment](#part-2-local-deployment)
- [Contributing](#contributing)
- [License](#license)
 
### Overview  
The objective of this project is to design and implement a **multimodal fake news detection pipeline** using the REDDOT model architecture. This involves leveraging both visual (image) and textual (caption) inputs to assess the authenticity of news content. By utilizing the pretrained RED-DOT classifier checkpoint and CLIP ViT-L/14 embeddings, the model is capable of jointly analyzing images and their associated captions to determine whether the news is **True** or **Fake**.


The project is divided into two parts:

### Part 1: Inference Script 
- Utilize the provided REDDOT model, trained checkpoint, and test datasets.
- Create an inference script that:
  - Accepts an image and caption. 
  - Predicts whether the news is **True** or **Fake**.
  - Outputs the **Confidence Score** and **Entropy Score**.
- Perform analysis and draw conclusions from the results.

#### Model Configuration
- Encoder: `CLIP ViT-L/14`
- Model Parameters:
  - `evidence = 0`
  - `neg evidence = 0`
  - `Tf layers = 4`
  - `Tf head = 8`
  - `Tf dim = 128`

*Note*: Follow the architecture strictly. Only additional modules may be modified.

---

### Part 2: Local Deployment

Deploy the inference pipeline from Part 1 as a local web application.

#### Backend
- **FastAPI** is used as the backend framework to serve the inference API.

#### Frontend
- **Streamlit** is used for the UI interface.

#### Frontend UI includes:
- Upload interface for image and caption.
- Display of:
  - Uploaded data
  - Inference time
  - Prediction (True/Fake)
  - Confidence Score
  - Entropy Score

#### Bonus
- Multi-sample input support.
- Results displayed in a clean, structured format.


## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvement, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to customize this README and code according to your project's specific details and requirements! 

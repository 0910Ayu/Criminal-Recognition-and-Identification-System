# Criminal-Recognition-and-Identification-System
The Criminal Recognition and Identification System (CRISYS) is an AI-based technology that creates detailed visual representations of suspects from textual descriptions. Combining NLP and GANs, CRISYS translates witness input into lifelike images, extracting details like facial features, eye color, and hairstyle. The system enhances criminal investigations by offering faster and more accurate suspect identification than traditional sketches. However, its implementation raises concerns about bias, privacy, and misuse, highlighting the need for ethical guidelines and data security. CRISYS has the potential to revolutionize law enforcement but requires careful ethical and operational oversight.

The challenge of accurately identifying criminal suspects has long existed, with traditional methods like witness descriptions and composite sketches often lacking precision. However, AI and machine learning are transforming this process. The Criminal Recognition and Identification System (CRISYS) uses natural language processing and generative modeling to create realistic images of suspects based on textual descriptions, such as eye color, hairstyle, and facial features. This system aims to bridge the gap between subjective descriptions and objective visual representations, improving lead generation, witness recall, and public safety. As AI continues to evolve, it holds great potential to revolutionize criminal identification.
                          Implementing AI systems like CRISYS in law enforcement presents challenges, including bias, privacy concerns, and ethical implications. This paper provides an overview of CRISYS, discussing its architecture, methodology, and potential applications, while also emphasizing the need to address ethical considerations. The study balances technical innovation with ethical responsibility, aiming to contribute to the discussion on AI’s responsible use in criminal justice. It stresses the importance of developing AI systems that are effective, fair, transparent, and respectful of individuals' rights.

![Screenshot 2025-05-07 123135](https://github.com/user-attachments/assets/b4907227-e8df-41bf-882c-f2a58313aee2)


Prompt-based generation models, like CRISYS, can be biased due to the datasets they rely on. To minimize this, diverse datasets and structured prompts are recommended. The FFHQ dataset from Kaggle, which offers a balanced demographic mix, is used to ensure fair image generation across various ethnicities and age groups.

## Key tools used include:
Stable Diffusion: For generating high-quality images from text prompts.
Prompt Condensation: A Python function that condenses user-defined attributes into effective prompts.
OpenCV: Converts generated images into pencil sketches for clarity evaluation.
Hugging Face Diffusers: Provides access to pre-trained models for text-to-image generation.
Kaggle: Sources the FFHQ dataset to ensure balanced and high-quality training data

## Problem Statement :-
 In the domain of criminal identification, law enforcement agencies frequently rely on witness
 testimonies to identify suspects. However, these testimonies are often plagued by unreliability.
 Factors such as stress, fear, and the passage of time can distort a witness’s recollection of events
 and details. Even when witnesses do recall the appearance of a suspect, there is considerable
 variation in their ability to articulate these details clearly and accurately. This inconsistency poses
 a significant challenge for forensic artists, who must interpret the descriptions and render them
 into sketches.
 The process of creating composite sketches is not only time-consuming but also inherently
 inconsistent, as it heavily depends on the artist's interpretation and skill level. This reliance on
 subjective interpretation can lead to sketches that fail to accurately capture the suspect's
 appearance. Such inaccuracies can hinder the investigative process, delaying the identification
 and apprehension of suspects.
 These limitations highlight the need for more reliable and efficient methods of suspect
 identification. By addressing these challenges, new technological solutions, such as the Criminal
 Recognition and Identification System (CRISYS), aim to enhance the accuracy and speed of the
 identification process, thus supporting more effective criminal investigations.

 ## Project Planning :-
 ![Screenshot 2025-05-07 122645](https://github.com/user-attachments/assets/fd4574da-b26c-4458-84b2-841910939030)


The **Criminal Recognition and Identification System (CRISYS)** aims to generate accurate facial sketches based on detailed verbal descriptions from witnesses or law enforcement.
### Description Processing
1. **Natural Language Processing (NLP)**: The system uses advanced NLP to extract specific facial features from descriptions (e.g., eye color, hair style).
2. **User Interface**: An intuitive interface for easy input of descriptions.

### Sketch Generation
3. **Image Generation Model**: Deep learning models, like Stable Diffusion, generate realistic sketches based on parsed descriptions.
4. **Feedback Integration**: Users can refine sketches, allowing iterative improvements.

### Performance
5. **Speed and Accuracy**: The system is designed to generate sketches quickly and accurately, handling a range of descriptions.
6. **Modular Design**: Components (e.g., interface, NLP, sketch generator) are modular for easy updates.

### Core Modules
* **Backend Server**: Manages data and processes user inputs.
* **Pencil Sketch Transformation**: Converts images into sketches.
* **Database**: Stores generated sketches securely.
* **Criminal Identification**: Optionally compares sketches with criminal databases.

### Ethical Considerations
* **Bias Mitigation**: Uses diverse datasets to ensure fairness.
* **Privacy Protection**: Adheres to strict data protocols.
* **Responsible Use**: Prevents misuse by establishing guidelines.

### Training Process
1. **Data Collection**: Utilizes the **FFHQ dataset** for facial images.
2. **Data Augmentation**: Enhances dataset diversity through techniques like rotation and brightness adjustment.
3. **Model Setup**: Uses a pre-trained model (e.g., Stable Diffusion) and fine-tunes it for the dataset.
4. **Training**: The model is trained with GPU acceleration and validated for performance.

### Generating and Refining Prompts
* **Objective**: Translate verbal descriptions into concise prompts for accurate image generation.
* **Optimization**: Refine prompts iteratively to ensure fidelity.

### Image Generation
* **Stable Diffusion**: The system generates detailed RGB images based on the refined prompts using GPU power for high resolution.

### Conversion to Sketch
1. **Grayscale Conversion**: The RGB image is converted to grayscale for focus on structure.
2. **Inversion & Gaussian Blur**: These techniques enhance light and shadow contrast, mimicking pencil strokes.
3. **Blending**: The inverted image is blended with the grayscale layer for a hand-drawn effect.
4. **Display**: Both the RGB image and the pencil sketch are shown side-by-side for comparison.
5. **Saving**: The final pencil sketch is saved as a high-quality PNG for clarity.

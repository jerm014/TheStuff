# Project 3028: Generative Adversarial Networks
----

## Resources

### Read or watch:

* [Original Paper on GANs](http://arxiv.org/pdf/1406.2661)
* [A Friendly Introduction to Generative Adversarial Networks (GANs)](https://www.youtube.com/watch?v=8L11aMN5KY8)
* [Google’s GAN course](https://developers.google.com/machine-learning/gan)
* [MIT 6.S191: Deep Generative Modeling - GANs](https://www.youtube.com/watch?v=yFBFl1cLYx8&t=1880s)
* [NYU Spring 2020 Week 9 Lecture on GANs](https://www.youtube.com/watch?v=Pgct8PKV7iw&t=5433s)
* [Dive into Deep Learning: Chapter 17. GANs](https://d2l.ai/chapter_generative-adversarial-networks/gan.html)
* [Stanford Graduate Course CS 236: Generative Adversarial Networks](https://cs236g.stanford.edu/)
* [GAN’s story so far](https://floydhub.ghost.io/gans-story-so-far/)
* [Towards Deep Generative Modeling With Weight & Biases](https://wandb.ai/ayush-thakur/keras-gan/reports/Towards-Deep-Generative-Modeling-With-Weight-Biases--Vmlldzo4MDI4Mw)
* [How to Implement Deep Convolutional Generative Adversarial Networks (DCGAN) in Tensorflow](https://wandb.ai/generative-adversarial-networks/dcgan-tensorflow/reports/How-to-Implement-Deep-Convolutional-Generative-Adversarial-Networks-DCGAN-in-Tensorflow--VmlldzoxNzkzNDg5?galleryTag=gan)
* [GAN’s visualized](https://poloclub.github.io/ganlab/)
* [Understanding GAN Loss Functions](https://neptune.ai/blog/gan-loss-functions)
* [Real-time visualizations of GAN learning and mode collapse](https://towardsdatascience.com/this-will-change-the-way-you-look-at-gans-9992af250454?gi=d2660b9212e3)
### Other links

* [Google Colab Notebooks](https://colab.research.google.com/)
  * Don’t forget to change runtime to a GPU!!!!

* [Weights and Biases Documentation](https://docs.wandb.ai/)
* [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
* [PyTorch Lightning Documentation](https://lightning.ai/docs/pytorch/stable/)
* [TensorFlow Documentation](https://www.tensorflow.org/api_docs)
* [Keras Documentation](https://keras.io/api/)
## Description

This course provides a hands-on experience in deep learning and GANs through two challenging projects. The first project focuses on Deep Convolutional GANs (DCGAN) with the MNIST dataset, while the second project allows you to tackle more complex image generation tasks using your choice of dataset, such as Celebrity Face Generation or Super-Resolution GANs. You will develop a solid understanding of GANs, experiment with various architectural and hyperparameter modifications, and gain proficiency in utilizing Weights and Biases for experiment tracking. The course will culminate in a final report summarizing your findings, insights, and project outcomes.

## Learning Objectives:

At the end of this project you are expected you are expected to be able to explain without the help of Google:

* **Environment and Framework Mastery:**Gain proficiency in setting up deep learning environments and working with popular deep learning frameworks (Tensorflow, PyTorch, or Keras).
* **Baseline Model Implementation**: Develop the ability to implement baseline GAN and DCGAN models for different projects.
* **Architectural Adaptation:**Learn how to modify GAN and DCGAN architectures, assessing their impact on image generation.
* **Hyperparameter Optimization:**Explore the effects of various hyperparameters, such as learning rates, batch sizes, and optimizers, on training stability and image quality.
* **Precision Management:**Experiment with precision changes (e.g., float32, float16, mixed-precision) and understand their impact on training speed and image generation quality.
* **Experiment Tracking:**Effectively utilize Weights and Biases (WandB) for comprehensive experiment tracking.
* **Project-Based Learning:**Choose and justify more complex image generation projects, applying knowledge from one project to another.
* **GitHub Repository Organization:**Efficiently structure and document your projects within GitHub repositories. *** Reflective Analysis:** Continuously reflect on and document key takeaways, insights, and observations throughout the course.

# Tips and Tricks for Task Video Submissions

In addition to the guidelines mentioned above, the following tips and tricks may help you improve the quality of your task demo video submissions and make the review process smoother and more efficient for your instructors.

- Before Recording
  - **Familiarize Yourself with Your Tools**: Understand the recording and editing software that you're using thoroughly. This knowledge can help you record more efficiently, add useful annotations, and produce higher quality videos.
  - **Prep Your Environment**: Clean up your desktop and browser tabs to avoid any unrelated content. If your recording software allows, consider highlighting the mouse cursor for better visibility during the demo.
  - **Prepare a Script or Outline**: Prepare a concise script or outline of what you will show and discuss in the video. This can help you stay on track and ensure all essential elements are covered.

- During Recording
  - **Speak Clearly**: If you are narrating, make sure you speak clearly and at a reasonable pace. You might find it helpful to practice your script or outline before recording.
  - **Be Concise but Comprehensive**: Your video should be brief but must still comprehensively demonstrate the functionality of the task. Keep your explanations simple and easy to understand.
  - **Show and Tell**: Do more than just tell what you've done; show it in action. Visual demonstration aids understanding and retention.

- After Recording
  - **Review Your Video**: Watch your video after recording to ensure all necessary parts are included and clear. Make sure the audio is clear and the video is not too fast or too slow.
  - **Edit If Necessary**: If your recording software has editing capabilities, take advantage of them to cut out unnecessary parts, add captions, or highlight key points.
  - **Choose the Right Platform for Sharing**: Ensure that the platform you choose for sharing your video is easily accessible by your instructors. Test the link before submission to confirm it works properly.

Remember that the purpose of the video is not just to demonstrate that you've completed the task, but also to clearly showcase your understanding and implementation of the project. Therefore, clarity and comprehension should be your main focus when recording.


## Requirements

### General

* Follow the PEP 8 coding style for Python[https://peps.python.org/pep-0008/](https://peps.python.org/pep-0008/)
* Employ Python’s default .gitignore in your holbertonschool-gan github repo

----
## Tasks
---
### 0. Deep Convolutional Generative Adversarial Network (DCGAN)

#### **Project Overview**
In this project, you will explore and experiment with the training of a Deep Convolutional Generative Adversarial Network (DCGAN) to generate images similar to the MNIST dataset. The primary objective is to gain practical experience in deep learning, specifically in GANs, by conducting a series of experiments using your preferred deep learning framework (TensorFlow, PyTorch, or Keras). We will utilize Weights and Biases to track and visualize the progress of these experiments.

#### **Project Tasks:**

- **Setup and Dataset (5 points)**
  - Set up your preferred deep learning framework (TensorFlow, PyTorch, or Keras) and create a working environment
  - Download the MNIST dataset and preprocess it for training and evaluation

- **Baseline DCGAN (5 points)**
  - Implement a baseline DCGAN architecture
  - Train the baseline DCGAN on the MNIST dataset

- **Experiment 1: Architecture Variations (10 points)**
  - Modify the DCGAN architecture (for example, number of layers, filter sizes, and strides)
  - Train the DCGAN with the modified architecture
  - Compare the results with the baseline

- **Experiment 2: Hyperparameter Tuning (15 points)**
  - Experiment with hyperparameters like learning rate, batch size, and optimizer choice
  - Record and analyze how hyperparameter changes affect training stability and image quality

- **Experiment 3: Precision Changes (10 points)**
  - Experiment with changing precision (for example, using float32, float16, or mixed-precision training if supported)
  - Observe how precision changes affect training speed and image generation quality

- **Weights and Biases Integration (15 points)**
  - Set up Weights and Biases (WandB) for experiment tracking
  - Log key metrics (such as generator and discriminator loss), hyperparameters, and images generated during each experiment

- **GitHub Repo Structure and Reasoning (10 points)**
  - Create a directory called dcgan inside inside holbertonschool-gan repo
  - Explain your chosen directory structure and the reasoning behind your organization
  - for e.g. an example structure

```
- dcgan/ - Root folder for the DCGAN project
  - data/ - Contains MNIST dataset and any preprocessed versions
  - models/ - DCGAN model architectures (baseline, experiment variations)
  - logs/ - Training logs and generated images from each experiment
  - experiments/ - Jupyter notebooks for each experiment
    - Separate notebooks allow tracking distinct experiments
  - utils/ - Helper scripts for data preprocessing, training, etc
  - configs/ - YAML files with model configs and hyperparameters
  - README.md - Overview of repo contents and documentation
```

- **Takeaways and Observation (30 points)**
  - After each experiment, write down your observations regarding model convergence, training time, image quality, and other relevant factors
  - Reflect on the challenges and insights gained from each experiment

- **Video Submission (30 points)**
  - Using Loom or OBS is generally the best way to record a video
  - Attach the link to the video in the doc
  - Create a 5 minute (or less) video that:
    - Provides an overview of what you did for the project, your reasoning behind decisions, and what you learned
    - Walks through the Weights & Biases dashboard, explaining the key metrics, hyperparameters, and results from each experiment
    - Highlights 2-3 main takeaways or observations from the experiments

#### **Project Deliverables:**
- Python code for each experiment and the baseline DCGAN
- Experiment logs in a Weights and Biases project
- A final report summarizing your observations, takeaways, and a discussion of which experiment(s) yielded the best results and why

**Repo:**

 - GitHub repository: `atlas-gan`
 - Directory: `dcgan`

---
### 1. Advanced GAN Experimentation for Complex Image Generation

#### **Project Overview**
In this advanced project, you will build upon your knowledge gained from the DCGAN MNIST project and dive into more complex challenges. Your task is to explore and experiment with Generative Adversarial Networks (GANs) in generating images for a more complex dataset. You have the flexibility to choose between projects like Celebrity Face Generation or Super-Resolution GANs. The project will continue to use your preferred deep learning framework (TensorFlow, PyTorch, or Keras) and Weights and Biases for tracking your experiments.

#### **Project Tasks:**

* **Project Selection (10 points)**
  * Chose a dataset and project of your choice
  * Should be more complex than MNIST, for e.g. Celebrity Face Generation (CelebA dataset) or Super-Resolution GANs(Div2K dataset)
  * Justify your choice based on what you learned from the DCGAN MNIST project

* **Setup and Dataset (5 points)**
  * Set up your deep learning environment with the chosen project in mind
  * Download the selected dataset and preprocess it for training and evaluation

* **Baseline GAN (5 points)**
  * Implement a baseline GAN architecture tailored to the chosen project
  * Train the baseline GAN on the complex dataset

* **Experiment 1: Architecture Variations (20 points)**
  * Modify the GAN architecture to optimize it for your chosen project
  * Train the GAN with the modified architecture
  * Compare the results with the baseline and highlight improvements

* **Experiment 2: Hyperparameter Tuning (25 points)**
  * Experiment with hyperparameters specific to your project (for example, layer depths, learning rates, kernel sizes, etc)
  * Record and analyze how these hyperparameter changes affect training stability and image quality for your project

* **Transfer of Knowledge (25 points)**
  * Reflect on how the lessons learned from the DCGAN MNIST project influenced your strategy in the current project
  * Discuss how your previous knowledge justified certain choices made in terms of architecture, hyperparameters, and training strategy

* **Weights and Biases Integration (15 points)**
  * Set up Weights and Biases (WandB) for experiment tracking
  * Log key metrics (such as generator and discriminator loss), hyperparameters, and images generated during each experiment

* **GitHub Repo Structure and Reasoning (10 points)**
  * Create a directory called advanced_gan inside holbertonschool-gan repo
  * Explain your chosen directory structure and the reasoning behind your organization
  * for e.g. an example structure
    * advanced_gan/ - Root folder for the DCGAN project
    * data/ - Contains dataset and any preprocessed versions
    * models/ - GAN model architectures (baseline, experiment variations)
    * logs/ - Training logs and generated images from each experiment
    * experiments/ - Jupyter notebooks for each experiment
      - Separate notebooks allow tracking distinct experiments
    * utils/ - Helper scripts for data preprocessing, training, etc
    * configs/ - YAML files with model configs and hyperparameters
    * README.md - Overview of repo contents and documentation

* **Takeaways and Observations (35 points)**
  * After each experiment, write down your observations regarding model convergence, training time, image quality, and other relevant factors
  * Reflect on the challenges, adaptations, and insights gained during this more complex project

* **Video Submission (50 points)**
* Using Loom or OBS is generally the best way to record a video
  * Attach the link to the video in the doc
  * Create a 5 minute (or less) video that:
    - Provides an overview of what you did for the project, your reasoning behind decisions, and what you learned
    - Walks through the Weights & Biases dashboard, explaining the key metrics, hyperparameters, and results from each experiment
    - Highlights 2-3 main takeaways or observations from the experiments

### **Project Deliverables:**

* Python code for each experiment and the baseline GAN
* Experiment logs in a Weights and Biases project
* A final report summarizing your observations, takeaways, and a discussion of how your knowledge from the DCGAN MNIST project influenced your approach to this more complex challenge


**Repo:**

 - GitHub repository: `atlas-gan`
 - Directory: `advanced_gan`


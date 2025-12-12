# Training Neural Networks using Congestion Control (AIMD)

## 1. Project Description
This project aims to test a novel hypothesis: applying the **AIMD (Additive Increase Multiplicative Decrease)** algorithm to neural network training.

The AIMD algorithm is famous for its role in internet stability (TCP protocol). Our idea is to adapt this "archaeological" mechanism (from 1989) to dynamically adjust the **Learning Rate** of a modern AI model. We consider an increase in error (loss) to be a "congestion" event, triggering a sharp decrease in the learning speed.

## 2. Data Used (EDA)
We are using the **CIFAR-10** dataset, a standard benchmark in Computer Vision.
* **Content:** 60,000 color images (32x32 pixels).
* **Classes:** 10 balanced classes (airplane, automobile, bird, cat, etc.).

Below are a few examples from the dataset that we analyzed:
<img width="787" height="100" alt="img1" src="https://github.com/user-attachments/assets/b6277391-8d94-4ac9-ab1a-e888165473ef" />


## 3. Model and Implementation
To establish a valid baseline for comparison, we implemented a basic model:
* **Architecture:** CNN (Convolutional Neural Network) with 3 convolutional layers.
* **Environment:** Google Colab (T4 GPU).
* **Files:** The source code can be found in the file `Project_ASI.ipynb`.

## 4. Intermediate Results (Baseline)
In this stage, we trained the standard model (without AIMD) to establish the baseline.
As observed in the graphs below, the model converges correctly, reaching an accuracy of over 70% in the first 10 epochs:

<img width="1003" height="389" alt="img2" src="https://github.com/user-attachments/assets/201483c0-56f6-4531-8be6-9a18b364d6bf" />


## 5. Roadmap (Next Steps)
1.  Implementation of the `AimdScheduler` class in Keras/TensorFlow.
2.  Running comparative experiments: Baseline vs. AIMD.
3.  Analysis of stability and convergence speed.

## References:

1.  **Archaeological Source (AIMD):** Chiu, D. M., & Jain, R. (1989). [Analysis of the increase and decrease algorithms for congestion avoidance in computer networks](https://www.cs.wustl.edu/~jain/papers/ftp/cong_av.pdf). Journal of Computer Networks and ISDN Systems.
2.  **Modern Deep Learning Context:** Smith, L. N. (2017). [Cyclical Learning Rates for Training Neural Networks](https://arxiv.org/abs/1506.01186). 
3.  **Dataset:** Krizhevsky, A. (2009). [The CIFAR-10 dataset](https://www.cs.toronto.edu/~kriz/cifar.html). University of Toronto.

# Syntharion
Overview
SYNTHARION is an artificial intelligence system designed to detect faint and fast-moving Near-Earth Asteroids (NEAs) that are often missed by traditional astronomical detection pipelines.

The project addresses a critical problem in planetary defense: identifying small, low-brightness objects before they pose a potential threat to Earth.
The system combines synthetic data generation with deep learning to significantly improve detection accuracy, reduce false positives, and accelerate data processing.

Key Features
• CNN architecture based on EfficientNet-B1
• Over 1,000,000 synthetic training samples
• 1.3σ detection threshold (more sensitive than standard 1.5σ)
• GPU-accelerated training
• 70% faster processing than traditional difference-imaging pipelines
• Extremely low false-positive rate (0.02%)

Motivation
Traditional detection systems rely on rule-based algorithms and classical difference imaging. These methods struggle with:
Dim asteroid streaks
High angular velocity objects
Limited labeled datasets
Large nightly data volumes (terabytes per night in surveys like ZTF)
Small asteroids often appear as faint elongated streaks that resemble noise. SYNTHARION addresses this blind spot using neural networks trained on realistic synthetic streak simulations.

Methodology
The detection pipeline includes:
Synthetic Data Generation
Real ZTF images used as background
Physically modeled asteroid streaks injected using PSF modeling
Balanced positive and negative samples
Deep Learning Model
EfficientNet-B1 backbone
TensorFlow / Keras implementation
Trained for 100 epochs using GPU acceleration

Detection Algorithm
Difference imaging
Noise standard deviation calculation
Thresholding at 1.3σ
CNN classification
Multi-detection filtering
Parameter Estimation
Apparent magnitude calculation
Angular velocity measurement
Orbit and size approximation

Results
Validation Accuracy: 99.8%
True Positive Rate: 97%
False Positive Rate: 0.02%
Processing Speed Improvement: 70%

The system detected six previously undiscovered asteroids in three nights of ZTF data, demonstrating real-world applicability.

Installation
Clone the repository:
git clone https://github.com/Ayau1ym/syntharion
cd syntharion
Install dependencies:
pip install -r requirements.txt

Recommended environment:
Python 3.10+
TensorFlow 2.x
NumPy
scikit-image

Running the Project
Run detection:
python asteroid_detection_algorithm.py

Train model:
python training_pipeline.py

Future Work
Real-time telescope integration
Orbit prediction module
Multi-wavelength analysis
Cloud-based detection service

Scientific Contribution
SYNTHARION demonstrates how synthetic data and deep learning can close detection gaps in asteroid monitoring while remaining computationally accessible. The project contributes to planetary defense research and supports Kazakhstan’s growing role in space innovation.

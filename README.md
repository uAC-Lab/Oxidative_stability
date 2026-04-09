

# Fatty Acid IP Predictor

A web application that predicts the **oxidative Induction Period (IP)** of oils from their fatty acid composition using a fine-tuned machine learning model. The model is described in the following publication: 

**Machine Learning-Based Inference of Oxidative Stability of Vegetable Oils** by Emmanuel Dike, Lucas Ayres, Justin Furgala, Jorge Barroso, Daniel Whitehead, and Carlos D. Garcia. _Journal of Food Composition and Analysis_ (2026) https://doi.org/10.1016/j.jfca.2026.109135


**Live Demo**: [https://oxidative-stability.up.railway.app/](https://oxidative-stability.up.railway.app/)

---

## Features
- Enter fatty acid compositions (C14:0, C16:0, C18:1, C18:2, C18:3, C20:1, C22:1)
- Quick presets for common oils (General, Soybean, Sunflower, Olive, Canola)
- Live validation — compositions must sum to 100%
- Prediction history table with all results


## How It Works
1. The user enters the weight percentage of 7 fatty acids
2. The backend computes **weighted molecular descriptors** (via RDKit) for the oil blend
3. It calculates derived features like **APE** (allylic position equivalents) and **BAPE** (bis-allylic position equivalents)
4. These 49 features are fed into a trained **XGBoost** model
5. The model returns the predicted **Induction Period** in hours
6. You are welcome to use the predictor, but we ask that you cite our work or give credit to it 

---

© Microanalytical Chemistry Lab — Clemson University

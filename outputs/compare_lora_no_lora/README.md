# Comparison: Baseline vs. LoRA

This folder contains side-by-side visual comparisons to demonstrate the effectiveness of the fine-tuned LoRA model in capturing the Megamendung batik pattern.

### 🎯 Objective
To directly compare the output of the base Stable Diffusion v1.5 model against the model enhanced with the Megamendung LoRA weight under identical conditions (same seed, prompt, and parameters).

### 📝 Experiment Setup
- **Prompt:** ("traditional Indonesian batik megamendung pattern, ""cloud motif, Cirebon style, textile design, high detail, 4k, red and black")
- **Base Model:** Stable Diffusion v1.5

### 📊 Visual Analysis

| Model | Pattern Accuracy | Style Consistency |
| :--- | :--- | :--- |
| **Baseline (No LoRA)** | **Failed.** Produces generic, noisy, or floral textures. | Inconsistent with Indonesian batik styles. |
| **With LoRA** | **Success.** Clearly renders the "cloud" (Megamendung) geometry. | High fidelity to the specific red-gradient cloud motifs. |

### 💡 Key Observation
The comparison proves that the LoRA model successfully injected the specific cultural concept of "Megamendung" into the latent space of Stable Diffusion. While the baseline model understands "batik" as a generic concept, only the LoRA-enhanced model can reconstruct the distinctive tiered cloud shapes and the traditional color palette of Cirebon's heritage.

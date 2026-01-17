# Seed Variation & Diversity Test

This folder demonstrates the **Generalization Ability** of the LoRA model by testing it across different random seeds.

### Objective
To prove that the model has truly learned the *concept* of Megamendung rather than just memorizing/copy-pasting a single image from the training data (overfitting).

### Experiment Setup
- **Prompt:** `traditional batik megamendung textile pattern`
- **LoRA Strength:** 1.0 (Optimal)
- **Seeds Tested:** `42`, `123`, `999`
- **Inference Settings:** 30 Steps, CFG 7.5

### Observations

| Seed | Key Features |
| :--- | :--- |
| **42** | Shows a vivid orange-on-blue contrast with very sharp, defined cloud borders.|
| **123** | Demonstrates a deep blue/indigo aesthetic, reminiscent of traditional natural dyes, with a more intricate, fine-lined texture. |
| **999** | Presents a more elongated and flowing interpretation of the clouds, showing the model understands the "directional" nature of the pattern. |

### Analysis: Generalization vs. Memorization
The results across different seeds show significant variations in composition, color distribution, and pattern flow. 
- **Not a "Copy-Paste":** If the model were overfitted, all three seeds would look nearly identical or distorted. 
- **Diverse Interpretation:** While each image is unique, they all consistently maintain the **fundamental geometry** of Megamendung (the tiered cloud shape). 
- **Conclusion:** This proves the LoRA is "robust"—it can generate an infinite variety of Megamendung patterns while staying true to the traditional aesthetic, making it useful for real-world design inspiration.

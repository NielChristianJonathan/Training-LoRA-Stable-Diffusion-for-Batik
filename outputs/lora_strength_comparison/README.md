# LoRA Strength Analysis (Weight Scaling)

This folder explores how the **LoRA Strength (Multipliers)** affects the balance between the base model's anatomy and the Megamendung pattern.

### Objective
To find the optimal weight (Alpha) that applies the Megamendung style without destroying the base image quality or over-saturating the features.

### Experiment Setup
- **Prompt:** (Same prompt as baseline for consistency)
- **Seeds:** Fixed to ensure the only variable is the strength.
- **Tested Strengths:** `0.6`, `1.0`, `1.4`

### Results & Observations

| Strength | Observation | Verdict |
| :--- | :--- | :--- |
| **0.6** | The pattern is faint. Only subtle hints of Megamendung "clouds" are visible. | **Underpowered** |
| **1.0** | **Optimal balance.** The pattern is clear, the colors are vibrant, and the image remains sharp. | **Sweet Spot** |
| **1.4** | The pattern is present, but the image is "fried," blurry, and loses structural integrity. | **Over-saturated** |

### Discussion: Overfitting vs. Over-saturation
This test demonstrates that the model is **not overfit** in a destructive way, but rather sensitive to weights:
1.  **Generalization:** At 0.6, the model still follows the base model's instructions, showing it hasn't "forgotten" everything else.
2.  **Stability:** The fact that 1.0 produces a clean image shows the training was successful.
3.  **Threshold:** The degradation at 1.4 is a common behavior in LoRA called *over-saturation*. It proves we have successfully mapped the pattern, and we now know the limit where the LoRA starts to conflict with the base model's weights.

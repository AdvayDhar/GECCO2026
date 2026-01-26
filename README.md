# Anonymous Research Code Repository

This repository contains the training, evaluation, ablation, ensemble generation, and Pareto front analysis code used in our paper.  
All experiments are conducted on two primary datasets:

- **MentalChat-16K:  ShenLab/MentalChat16K**
- **Auxiliary Career Guidance Dataset:  advy/career-guidance-counsellor-QA**

The repository is maintained in an anonymous format for review purposes.

---

## Repository Structure and File Descriptions

### Model Training

- **`6ModelTrain.py`**  
  Training script for the six base language models on the **MentalChat-16K** dataset.

- **`6ModelTrainAuxi.py`**  
  Training script for the same six base language models on the **auxiliary Career Guidance dataset**.

- **`AltLlamaTrainMentalChat16k.py`**  
  Fine-tuning / training code for the **LLaMA 71B model** on the **MentalChat-16K** dataset, as used in the paper. This is an alternate code, in case 6ModelTrain.py fails during Llama phase.

---

### Ablation Studies

- **`AblationMentalChat16k.py`**  
  Code used to run the ablation experiments described in the paper on the MentalChat-16K dataset.

- **`AblationResults.txt`**  
  Generated responses and outputs from the ablation experiments.

---

### Ensemble Generation and Evaluation

- **`EnsembleResponseGeneratorMentalChat.py`**  
  Core ensemble response generation pipeline.  
  This script includes the **two-stage combiner function** described in the paper and produces the final ensemble outputs.

- **`EnsembleResponsesMentalChat.txt`**  
  Generated ensemble responses on the **MentalChat-16K** dataset.

---

### Single-Model Outputs (LLaMA 71B)

- **`LlamaResponsesMentalChat16k.txt`**  
  Responses produced by the LLaMA 71B model on the **MentalChat-16K** dataset.

- **`LlamaCareerGuidanceResponses.txt`**  
  Responses produced by the LLaMA 71B model on the **auxiliary Career Guidance dataset**.

---

### Pareto Front Analysis

- **`Pareto3DCareerGuidance.html`**  
  Interactive 3D visualization of the Pareto front for the **Career Guidance dataset**.

- **`ParetoFront3DMentalChat.html`**  
  Interactive 3D visualization of the Pareto front for the **MentalChat-16K** dataset.

- **`ParetoFrontCareerGuidance.csv`**  
  CSV file containing Pareto-optimal points for the Career Guidance dataset.

- **`ParetoFrontMentalChat.csv`**  
  CSV file containing Pareto-optimal points for the MentalChat-16K dataset.

- **`ParetoFrontGenCareerGuidance.py`**  
  Code to generate the full Pareto front from the **five fine-tuned ensemble models** on the Career Guidance dataset.

- **`ParetoFrontGenMental16k.py`**  
  Code to generate the Pareto front from the **MentalChat-16K** dataset.

---

### Demo

- **`demo.mp4`**  
  A short demonstration video showcasing a lightweight frontend of the ensemble inference workflow.

---

## Notes

- This repository is intended **solely for reproducibility and evaluation** of the experiments described in the paper.
- The codebase is intentionally anonymized for double-blind review.


If this repository is used, please cite the corresponding paper (citation details will be provided upon publication).

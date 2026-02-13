# TOPSIS Analysis of Pre-Trained Text Conversational Models

This repository contains the implementation of the TOPSIS (Technique for Order Preference by Similarity to Ideal Solution) method to identify the best pre-trained Conversational AI model based on multiple evaluation criteria.

This work has been completed as part of an academic assignment focused on applying multi-criteria decision-making techniques to compare modern AI systems.

---

## Assignment Objective

To apply the TOPSIS method to evaluate and rank pre-trained NLP models across different performance and efficiency parameters and determine the most optimal model overall.

---

## Domain Selected

Text Conversational AI  
(Roll number ending with **4**)

---

## Models Evaluated

The following popular conversational AI models were analysed:

- GPT-2 Medium (Dialogue-tuned)
- GPT-Neo 1.3B
- BLOOM-560M
- FLAN-T5 Base
- OPT-1.3B
- LaMDA-Style Model

---

## Evaluation Criteria

Each model was evaluated on multiple quantitative criteria:

| Criteria | Description | Nature |
|--------|------------|--------|
| Response_Relevance | Quality and relevance of generated responses | Benefit |
| Context_Retention | Ability to retain multi-turn conversational context | Benefit |
| Inference_Time_ms | Response generation latency | Cost |
| Model_Size_MB | Storage and deployment footprint | Cost |
| Training_Data_Size_GB | Size of pre-training dataset | Benefit |
| Energy_Consumption_kWh | Computational energy requirement | Cost |

Benefit criteria increase the score, while cost criteria decrease it.

---

## Raw Dataset

| Model | Response_Relevance | Context_Retention | Inference_Time_ms | Model_Size_MB | Training_Data_Size_GB | Energy_Consumption_kWh |
|------|------------------|------------------|------------------|--------------|----------------------|------------------------|
| GPT2_Medium_Dialogue | 0.80 | 0.75 | 95 | 1500 | 40 | 50 |
| GPT_Neo_1.3B | 0.83 | 0.80 | 140 | 2600 | 800 | 75 |
| BLOOM_560M | 0.82 | 0.78 | 120 | 1100 | 350 | 65 |
| FLAN_T5_Base | 0.85 | 0.82 | 100 | 990 | 780 | 60 |
| OPT_1.3B | 0.84 | 0.81 | 145 | 2500 | 180 | 80 |
| LaMDA_Style_Model | 0.88 | 0.86 | 160 | 2800 | 1000 | 90 |

---

## Weights and Impacts Used

Weights represent the importance of each criterion in decision making.

### Weights

0.25, 0.25, 0.15, 0.10, 0.15, 0.10

### Impacts

+, +, -, -, +, -


---

## Methodology

TOPSIS analysis was performed using a Python implementation that automates the complete TOPSIS workflow including:

- Normalization of decision matrix
- Weighted normalization
- Ideal best and ideal worst calculation
- Euclidean distance computation
- Relative closeness score
- Final ranking

---

## How the Analysis Was Executed

The analysis was executed using Python by providing the dataset, weights, and impacts as input.

```bash
python TopsisforPretrainedModels.py \
text_conversational_models.csv \
"0.25,0.25,0.15,0.10,0.15,0.10" \
"+,+,-,-,+,-" \
result.csv

This command generated the final TOPSIS scores and rankings.
```
---

## Output

The result file contains two additional columns:

- Topsis Score
- Rank

Higher TOPSIS score indicates better overall performance relative to the ideal solution.

---

## Graphical Analysis

To support the decision visually, multiple graphs were generated, including:

- TOPSIS score comparison bar graph
- Criteria-wise performance graphs

All visualizations are available inside the repository.

---

## Conclusion

TOPSIS provides a systematic framework to evaluate conversational AI models across multiple dimensions rather than relying on a single benchmark.

Based on the computed scores, models are ranked according to their closeness to the ideal best solution and distance from the ideal worst solution.

---

## Author

Aishita Kumar

Roll No.: 102303744


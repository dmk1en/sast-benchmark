# SAST Tool Evaluation Report

## Metadata Expansion
Per-entry triage fields added:
* **Vulnerabilities bucket:** `vulnerabilities[]` &rarr; `my_verdict`, `my_explain`
* **False-positives bucket:** `false_positives[]` &rarr; `my_verdict`, `my_notes`

---

## Tool Result Stats

### 1. Vulnerabilities Bucket
*Tool flagged these as **real** (n = 53)*

| My Verdict | Count |
| :--- | :--- |
| **TRUE POSITIVE** | 40 |
| **FALSE POSITIVE** | 9 |
| **MIXED** | 4 |

### 2. False-Positives Bucket
*Tool flagged these as **dismiss** (n = 38)*

| My Verdict | Count |
| :--- | :--- |
| **FALSE POSITIVE** *(Tool was right)* | 24 |
| **TRUE POSITIVE** *(Tool missed / Leak)* | 11 |
| **MIXED** | 3 |

---

## Confusion Matrix
*Note: Mixed entries ($n = 7$) are excluded from the matrix ($n = 84$).*

| | Actually Vuln | Actually Not |
| :--- | :---: | :---: |
| **Tool Flagged** | **TP** = 40 | **FP** = 9 |
| **Tool Dismissed** | **FN** = 11 | **TN** = 24 |

---

## Performance Metrics

* **Precision:** $rac{40}{49} = 81.6\%$
* **Recall:** $rac{40}{51} = 78.4\%$ *(was 80.0% — final flip added 1 FN)*
* **F1-Score:** $80.0\%$
* **Accuracy:** $rac{64}{84} = 76.2\%$
* **Mixed Cases:** 7 entries *(excluded from primary statistical metrics)*

# SOFL-CoT Benchmark Dataset

This repository contains four structured datasets formatted using **SOFL-CoT** (Structured Object-Oriented Formal Language - Chain of Thought) methodology. Each dataset provides:

- A natural language requirement (`requirement`)
- A structured formal specification in SOFL-like reasoning style (`sofl_cot`)
- A code implementation (`code`)
- Associated programming language label (`language`)

---

## 📊 Dataset Statistics

| Dataset Name | Language | # Samples | Avg. Code Length | Avg. Requirement Length | Avg. SOFL-CoT Length |
|--------------|----------|-----------|------------------|--------------------------|-----------------------|
| humaneval | Python | 164 | 175.5 | 448.5 | 409.3 |
| mbcpp | cpp | 848 | 172.6 | 77.7 | 403.5 |
| mbpp_python | Python | 974 | 180.6 | 78.6 | 413.7 |
| mbpp_java | Java | 974 | 240.0 | 78.6 | 414.1 |


---

## 📁 Dataset Structure

Each `.jsonl` file contains a list of entries with the following structure:

```json
{{
  "id": "string",
  "language": "Python | Java | cpp",
  "requirement": "Natural language description of the task",
  "sofl_cot": "Formal step-by-step reasoning in SOFL style",
  "code": "Source code solution"
}}
```

---

## 🗃️ Available Merged Datasets

- `sofl_cot_merged_python.jsonl` — All Python-based tasks  
- `sofl_cot_merged_java.jsonl` — Java-converted and Java-native samples  
- `sofl_cot_merged_cpp.jsonl` — C++ tasks derived from MBCPP  

---

## 📜 Citation

If you use this dataset, please cite as:

```bibtex
@misc{soflcot2025,
  title = {{SOFL-CoT}: A Multi-language Dataset for Formal Reasoning and Code Generation},
  author = {{Yuxiang Shang}},
  year = {2025},
  howpublished = {\url{{https://github.com/Seansyx123/SOFL-CoT-dataset}}},
  note = {Version 1.0}
}
```

---

## 🔗 License

This dataset is released under the MIT License.



---

## 🔄 Additional Dataset: MBPP (Python → Java Conversion)

We also provide a converted version of the [MBPP dataset](https://github.com/google-research/google-research/tree/master/mbpp), where each Python solution has been translated into Java-style code for cross-language training or comparison purposes.

- 📁 File: `mbpp_java_style_code.jsonl`
- 🧾 Fields:
  - `task_id`: Original MBPP task ID
  - `text`: Task description (requirement)
  - `code`: Java-style pseudo-code converted from Python

Note: Some loop structures may include placeholder comments such as `// [manual conversion needed for loop]` and require manual refinement for full Java compilation.


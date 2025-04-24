# Viamo DPG Open Data

This repository hosts open datasets shared by Viamo as digital public goods. Our goal is to contribute to the United Nations' Sustainable Development Goals by making valuable data accessible.

## Data Sharing and Accessibility

* **License**: Datasets in this repository are released under CC-BY-4.0 license; see the `LICENSE` file for the full legal text.
* **Format**: Data is provided in JSON (`.json`), a standard, open format accessible with many programming languages and tools.
* **Access**: The data can be accessed directly from this GitHub repository, i.e., https://github.com/ViamoInc/DPG

## Datasets

### GIZ Project Data for India and Kenya

#### Summary

This dataset contains anonymized questions and responses collected via Viamo's automated voice lines in India and Kenya between March 2024 and April 2025, provided in JSON format. It includes only interactions successfully transcribed by an automated speech recognition (ASR) system; interactions deemed unintelligible by the ASR (e.g., due to background noise or poor audio quality) are excluded.

The files are organized as follows:
```
.
├── giz/
│   ├── giz_india.json      # Data specific to India
│   └── giz_kenya.json      # Data specific to Kenya
```

#### Data Dictionary / Schema

The data within each `.json` file is structured as an array of objects. Below is a description of the key fields, their data types, definitions, and units where applicable:

**Example:**

```json
[
  {
    "id": 1193684,
    "input": "Where can I buy maize seed in <LOCATION>?",
    "response": "You can buy maize seed from agrodealers in <LOCATION>. They are the main suppliers for farmers in the area."
  }
  // ... more records
]
```

**Field Descriptions:**

* **`id`**:
    * **Type**: Integer
    * **Description**: Unique ID of a question-response pair
    * **Allowed Values / Format**: Positive integer
* **`input`**:
    * **Type**: String
    * **Description**: Transcript of the caller's question
* **`response`**:
    * **Type**: String
    * **Description**: Transcript of the system's response

# Chat_Bot
# Mini Conversational AI Chatbot Dashboard

## Project Overview
This project is an End Semester Laboratory Examination Submission aimed at designing, implementing, and analyzing a multi-turn conversational AI chatbot using Hugging Face Transformers and Gradio. The system specifically evaluates and compares two models—**TinyLlama (1.1B)** and **GPT-2**—running within the constraints of the Google Colab Free Tier environment.

---

## Architectural Design
* **Core Processing Engine:** Features a dual-model architecture utilizing `TinyLlama/TinyLlama-1.1B-Chat-v1.0` and `gpt2`.
* **State Management:** Utilizes linear multi-turn conversation memory buffers to preserve local temporal context during chats.
* **Telemetry Layer:** Incorporates high-resolution timers and memory diagnostic wrappers to compile real-time comparative dataframes.
* **Interface Layer:** Deploys a dynamic, web-based interface built with Gradio that features real-time hyperparameter adjustments.

---

## Key Features & Experiments
* **Dynamic Hyperparameter Tuning:** The interface allows users to adjust parameters such as Temperature, Max New Tokens, Top-K, Top-P, and Repetition Penalty in real-time.
* **Live Performance Logging:** The Gradio interface includes a "Live Performance Log Engine" that tracks the selected model's response time, response length, and RAM usage dynamically.
* **Automated Analysis:** The system is capable of running automated experiments to compare inference latency and response sequence lengths across different hyperparameter sweeps (e.g., low variance vs. high variance).

---

## Model Analysis & Structural Observations
Based on the experimental analysis, the following structural observations were made:
* **TinyLlama (1.1 Billion parameters):** Provides dramatically more coherent and instructional responses due to its larger parameter size and specific chat/instruction fine-tuning. 
* **GPT-2 (124 Million parameters):** Operates extremely fast and is very lightweight, but it occasionally rambles, loses context, and struggles with logical multi-turn dialogue without highly specific few-shot prompting.

### Model Comparison Matrix

| Feature Criterion | TinyLlama-1.1B-Chat | GPT-2 (Base) |
| :--- | :--- | :--- |
| **Parameter Count** | ~1.1 Billion | ~124 Million |
| **Memory Profile** | High (~2.5 GB in fp16) | Very Low (~600 MB) |
| **Context Strength** | Strong chat formatting and logic | Weak context tracking |
| **Latency Profile** | Slower, dense computation | Extremely fast generation |

---

## System Completion Status
* Multi-model deployment achieved successfully on the Colab Free tier.
* Contextual memory systems successfully mapped to both models' requirements.
* Interactive Gradio execution environment deployed successfully.

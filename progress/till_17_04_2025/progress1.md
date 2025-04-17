# Megha's Progress

Explored how AI-powered WAFs can be built using BERT to classify malicious HTTP requests such as SQL Injection, XSS, Command Injection, etc.

Researched and finalized the "CICIDS2017 dataset" for modeling. It contains both normal and multiple attack types like:
- DoS Hulk
- Heartbleed
- Web Attack – SQL Injection, XSS
- Brute Force, DDoS, and more.

Preprocessed the dataset in Pandas — handled missing values and cleaned all column names (used `df.columns.str.strip()` to remove whitespaces).

Converted key request features like Source IP, Destination IP, Port, and Protocol into "natural language format" to make it compatible with Hugging Face models.

Set up Hugging Face tokenizer and created a `Dataset` object for training.

Loaded the `bert-base-uncased` model with a classification head.

Defined training arguments and used Hugging Face’s `Trainer` to begin fine-tuning.
![image](https://github.com/user-attachments/assets/9b11e7fd-32a7-46f6-ad67-d19305267e7f)


Training is in progress right now — it’s slow due to CPU-based execution. Might need to move to Google Colab or use GPU for faster training later.

## Current Requirements / Notes
- Training takes significant time locally — might move to Google Colab
- Will explore using FastAPI for serving predictions after training completes


# Paraphrase-Generation-System-Using-T5-hugging-Face-Model

# 1. Project Overview

This project uses the T5 (Text-to-Text Transfer Transformer) model to generate paraphrases of input sentences. The system converts input text into token IDs, processes them through a pretrained/fine-tuned T5 model, and then converts the output numbers back into human-readable text.

# 2. Main Components
## a) Tokenizer
A pretrained T5 model (e.g., t5-base) that performs text-to-text tasks.

Processes tokenized input and predicts output sequences.

Can be fine-tuned specifically for paraphrasing tasks.
# b)Model
A pretrained T5 model (e.g., t5-base) that performs text-to-text tasks.

Processes tokenized input and predicts output sequences.

Can be fine-tuned specifically for paraphrasing tasks.
# c) Device Management
The model and inputs can be moved to CPU or GPU.

GPU usage significantly speeds up training and generation.

# D) Training Configuration
Uses training arguments to control:

    Learning rate

    Batch size

    Number of epochs

    Logging and checkpointing

Ensures efficient, reproducible, and optimized training.

# E) Tokenization Function
Prepares input and target text for the model.

Applies padding and truncation for uniform sequence lengths.

Creates labels for the model to learn during training.

# F) Pharaphrase
Input text is preprocessed with a task prefix (e.g., "paraphrase: ").

Uses tokenizer to convert text to token IDs.

Model generates outputs, which are then decoded back to text.

# Work Flow
Input Text → Preprocessed with a prefix like "paraphrase: ".

Tokenizer → Converts text to token IDs.

Model → Processes token IDs using learned weights and generates output IDs.

Tokenizer → Converts output IDs back to readable text.

Output → Returns a list of paraphrased sentences

# Improving Paraphrase Diversity
Enable sampling with do_sample=True.

Increase top_k and top_p to allow more token choices.

Increase temperature slightly for more creative outputs.

Avoid too high beam search if diversity is desired.

# Saving and loading model
Save model and tokenizer separately for future use:

Model → contains learned weights

Tokenizer → contains vocabulary and tokenization rules

Both are required for consistent inference on new sentences.


# Key Takeaways
Tokenizer is essential before and after the model.

Beam search improves quality but reduces diversity.

Sampling and temperature control creativity and variability.

Proper configuration balances quality, speed, and diversity of paraphrases.


# Context-Aware Sarcasm Detection via Hierarchical Transformer Encoding and Attention-Based Context Modeling

## Overview

Sarcasm detection is a challenging Natural Language Processing (NLP) task due to its strong reliance on conversational context. Many sarcastic utterances appear neutral or even positive when analyzed in isolation, making contextual understanding essential for accurate classification.

This project presents a **context-aware deep learning framework** that preserves the complete conversational structure through hierarchical transformer-based encoding and attention-driven context modeling. Unlike approaches that summarize conversation history into a compressed representation, the proposed method processes each utterance individually, enabling richer modeling of contextual dependencies and reducing information loss.

---

## Abstract

Sarcasm detection remains a challenging problem in Natural Language Processing due to its strong dependence on contextual understanding. Isolated utterances often lack sufficient information to accurately determine sarcasm, making effective context modeling essential.

This project proposes a context-aware framework that preserves the full conversational structure using a hierarchical architecture. Each utterance is encoded using a transformer-based model, followed by a context encoder that captures inter-sentence relationships within the conversation. An attention mechanism is then applied to dynamically identify the most relevant contextual cues for sarcasm detection.

The resulting context representation is combined with the target utterance and passed to a classifier for final prediction. This approach avoids information loss introduced by summarization methods and enables more precise modeling of contextual dependencies.

The model is evaluated using standard classification metrics, including **F1-score**, **Accuracy**, and **Jaccard Coefficient**, with the goal of improving robustness and contextual understanding in sarcasm detection tasks.

---

## Architecture

### 1. Utterance Encoder

Each utterance within a conversation is independently encoded using a pretrained transformer language model (e.g., DeBERTa or DistilBERT), producing contextualized sentence embeddings.

### 2. Context Encoder

The sequence of utterance embeddings is processed by a higher-level transformer encoder that captures relationships between conversation turns and models discourse-level context.

### 3. Attention-Based Context Selection

An attention mechanism identifies the most relevant contextual utterances for the target statement, allowing the model to focus on information that contributes most strongly to sarcasm interpretation.

### 4. Classification Layer

The attended context representation is combined with the target utterance representation and passed through a feed-forward neural network for binary sarcasm classification.

# ai-tutor
A System Prompt for College-Level Instruction

**Author:** Ariel Stilerman  
**Affiliation:** Department of East Asian Languages and Cultures, Stanford University  
**Date:** February 8, 2026

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Gemini Gem Ready](https://img.shields.io/badge/Gemini_Gem-Ready-blue.svg)](https://gemini.google.com/gems/view)

---

## 📋 Abstract

> This project introduces a new AI tutoring framework designed to align with the pedagogical values of a liberal arts education. Addressing the tendency of generic Large Language Models (LLMs) to bypass student effort through over-explanation, this project proposes a design strategy based on **prompt engineering**. 
>
> By limiting model outputs and enforcing a Socratic questioning method, the tutor prioritizes student active understanding over rapid answers. This repository provides a generalized template that allows instructors in any field to create specific pedagogical workflows while retaining the core architecture that turns an LLM into an effective tutor.
>
> The tutor was originally developed for Premodern Japanese (and still available as open-source on /bungo-bot repository). 

---

## 1. Introduction

The promise of AI to save effort can often backfire. Advertisements for tools like Anthropic's Claude invite users to *"Do five things while you focus on one,"* suggesting we can bypass the messy, confusing experience of completing homework and preparing course materials for class by delegating it to an LLM. However, a liberal arts education advocates for the opposite: it challenges us to read/study more slowly and write/solve more deliberately. 

College represents a unique opportunity to cultivate the complex intellectual habits that will sustain us later. This raises a critical question: **how can we design AI tools that align with these values, where effort and process are inseparable from outcome and performance?**

This project proposes a tutor designed to augment, not replace, the instructor. The tutor guides students as they work through a text or problem using targeted questions and contextual explanations. 

Consequently, the tutor discussed here is designed for students enrolled in formal courses; it isn't intended for self-taught learners or as a replacement for human instruction.

## 2. Context of Use and Need

A tutor built on top of an LLM can address the primary barrier to entry for students: the steep learning curve of independent analysis. 

Generic LLMs do not come ready out-of-the-box for pedagogic applications. They are good at providing information, but not necessarily at tutoring. Common failures include:
* **Context Drift:** Losing track of original instructions as the conversation progresses.
* **Information Dumping:** Answering simple questions with dense multi-paragraph blocks.
* **Hallucination:** Confidently offering false or misleading information.
* **Reactive Stance:** Responding to prompts rather than guiding the learning arc.

The system prompt we propose is designed to compel the model to abandon its common function of providing direct answers.

## 3. Prompt Engineering Architecture

To ensure the tutor behaves consistently, we use a system prompt written in natural language and organized with XML tags. This modular approach allows for easy adaptation ("forking") to other subjects.

## 4. Design Strategy

Building a tutor that guides students through active analysis can be achieved in different ways. Retraining with high-quality task-specific data (supervised fine-tuning) or expanding its knowledge base (RAG) is expensive and requires expertise in machine learning.

By contrast, **System Prompt Engineering** is an inexpensive, highly scalable approach. 

Testing in late 2025 and early 2026 showed **DeepMind's Gemini 3** offers a suitable foundation model.
Other models, such as OpenAI's ChatGPT 5.2, showed a tendency to over-explain and rush ahead, while xAI's Grok lacked necessary customization features.



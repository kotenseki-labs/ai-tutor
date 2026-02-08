# ai-tutor
A System Prompt for College-Level Instruction

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Gemini Gem Ready](https://img.shields.io/badge/Gemini_Gem-Ready-blue.svg)](https://gemini.google.com/gems/view)


## 📖 Overview

> This project introduces a new AI tutoring framework designed to align with the pedagogical values of a liberal arts education. Addressing the tendency of generic Large Language Models (LLMs) to bypass student effort through over-explanation, this project proposes a design strategy based on **prompt engineering**. 
>
> By limiting model outputs and enforcing a Socratic questioning method, the tutor prioritizes student active understanding over rapid answers. This repository provides a generalized template that allows instructors in any field to create specific pedagogical workflows while retaining the core architecture that turns an LLM into an effective tutor.
>
> The tutor was originally developed for Premodern Japanese (and still available as open-source on /bungo-bot repository). 


**AI-Tutor** is not an app, but a specialized **System Prompt** designed to transform a standard LLM (specifically Gemini Gems) into an "active leraning" tutor for college-level courses.

## 📂 Repository Structure

* `system_prompt.xml` - **This is the core file**: Copy the contents of this file into your customized AI instructions box (e.g. your Gemini Gem).
* `examples/` - Sample tutors for different fields.

## ♊ How to Use (Gemini Gems)

You do not need to install Python or run any code. Follow these steps to create your own tutor:

1.  **Open Gemini:** Go to [gemini.google.com](https://gemini.google.com).
2.  **Create a Gem:** Click on "Gem manager" $\to$ "New Gem". 
3.  **Name It:** Give it a name like "Tutor for {COURSE_NAME}]"
4.  **Copy the Prompt:**
    * Open the [`system_prompt.xml`](system_prompt.xml) file in this repository.
    * Copy the entire text and paste into the "Instructions" field of your new Gem.
    * Replace COURSE_TOPIC_AND_SCOPE at the top of the prompt with your course title or field.
6.  **Save & Chat:** Click "Create". Your tutor is now ready to use for you and your students!

## 🛃 Customizing the Tutor

The prompt is written in natural language wrapped in XML tags. You can modify the behavior by editing the text before you paste it. For example:

* **Adjusting Pace:** 
    * *Current:* "Ask one question at a time."
    * *Change to:* "Ask up to three questions" (if you want a faster pace or options for the student to pick from).
* **Changing Tone:** 
    * You can add instructions like "Be strict but encouraging"
    * You can change the interaction language to Spanish.

## 🛠️ How to Contribute

We use GitHub to version-control the system prompt of BungoBot. Here is how you can help:

* **Fork & Clone:** Fork this repo and create a new branch for your feature or fix.
* **Edit Instructions:** Make changes to the system prompt in `system_prompt.xml`
* **Test Locally:** Copy the system prompt from `system_prompt.xml` into your own [Gemini Gem](https://gemini.google.com) and test intesively to verify the tutor behaves as expected and doesn't crash.
* **Submit a PR:** Push your changes and open a Pull Request. Please include:
    * **The Change:** What specific instructions or features did you add/remove?
    * **The "Why":** Did the tutor performance improve? How?
    * **Example Output:** (Optional) A screenshot or text snippet of the tutor's response using the new system prompt.


## 🧠 Project Rationale

The promise of AI to save effort can often backfire. Advertisements for tools like Anthropic's Claude invite users to *"Do five things while you focus on one,"* suggesting we can bypass the messy, confusing experience of completing homework and preparing course materials for class by delegating it to an LLM. However, a liberal arts education advocates for the opposite: it challenges us to read/study more slowly and write/solve more deliberately. 

College represents a unique opportunity to cultivate the complex intellectual habits that will sustain us later. This raises a critical question: **how can we design AI tools that align with these values, where effort and process are inseparable from outcome and performance?**

This project proposes a tutor designed to augment, not replace, the instructor. The tutor guides students as they work through a text or problem using targeted questions and contextual explanations. 

Consequently, the tutor discussed here is designed for students enrolled in formal courses; it isn't intended for self-taught learners or as a replacement for human instruction.

## 💦 Context of Use and Need

A tutor built on top of an LLM can address the primary barrier to entry for students: the steep learning curve of independent analysis. 

Generic LLMs do not come ready out-of-the-box for pedagogic applications. They are good at providing information, but not necessarily at tutoring. Common failures include:
* **Context Drift:** Losing track of original instructions as the conversation progresses.
* **Information Dumping:** Answering simple questions with dense multi-paragraph blocks.
* **Hallucination:** Confidently offering false or misleading information.
* **Reactive Stance:** Responding to prompts rather than guiding the learning arc.

The system prompt we propose is designed to compel the model to abandon its common function of providing direct answers.

## 🏠 Prompt Engineering Architecture

To ensure the tutor behaves consistently, we use a system prompt written in natural language and organized with XML tags. This modular approach allows for easy adaptation ("forking") to other subjects.

## ✏️ Design Strategy

Building a tutor that guides students through active analysis can be achieved in different ways. Retraining with high-quality task-specific data (supervised fine-tuning) or expanding its knowledge base (RAG) is expensive and requires expertise in machine learning.

By contrast, **System Prompt Engineering** is an inexpensive, highly scalable approach. 

Testing in late 2025 and early 2026 showed **DeepMind's Gemini 3** offers a suitable foundation model.
Other models, such as OpenAI's ChatGPT 5.2, showed a tendency to over-explain and rush ahead, while xAI's Grok lacked necessary customization features.

## 📄 License

This project is licensed under the **GNU General Public License v3.0** - see the [LICENSE](LICENSE) file for details. This ensures the project remains free and open for all students and scholars. Any modifications or derivative versions that you distribute must also be open source.

---

*Maintained by Ariel Stilerman @ Stanford University.*




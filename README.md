# Evaluating-GPT-Protected-Class-Biases

### 0. Starting

To run the experiment as described, you must make a copy of `.env-example` named `.env` and add your own OpenAI API key. The key mus have all permissions to submit jobs and read them for the **gpt-4o-mini-2024-07-18** model. You must also have money in your account. This experiment took under $0.40 to run.

### 1. Generating Prompts

Prompts for each of the two experiments were generated in `generate-prompts.ipynb`. The two sections of generation are labeled. This will create JSON files in the `json_data` folder for future code to access. This file depends on the completion of step 0.

### 2A. Classes to Stories

The `classes_to_stories.ipynb` file will take the previously generated classes and use the **gpt-4o-mini-2024-07-18** model to generate stories and evaluate their sentiment. All steps are laid out in the file with headings. This section depends on the completion of step 1.

### 2B. Stories to Classes

Using previously generated stories, `stories_to_classes.ipynb` will call the **gpt-4o-mini-2024-07-18** model to label each story with a variety of classes. This requires the completion of step 1.

### 3. Analyzing and Visualizing Data

After all of the data in the previous steps is generated, use `analyze_data.ipynb` to graph the data for easy analysis and understanding. This depends on all previous steps.
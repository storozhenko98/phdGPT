# README.md

## Project Title:
phdGPT: A Specialized Article Summarizer

## Description:
phdGPT is a Python-based tool tailored to automatically summarize PDF articles, with a specialized focus on articles in analytic philosophy. Utilizing the advanced capabilities of OpenAI's GPT-3.5 Turbo model, phdGPT generates summaries that are comprehensive, coherent, and technical, ensuring the preservation of complexities and intricate details inherent to the subject matter. This tool is invaluable for researchers and students, especially those undertaking PhD projects, who need a precise and meticulous understanding of varied articles.

## Features:
1. **PDF Text Extraction:**
   Efficiently extracts text from PDF articles stored in a designated directory.

2. **Adaptive Chunking:**
   Divides lengthy articles into manageable chunks to maintain contextual relevance during summarization.

3. **Analytic Philosophy Focused Summarization:**
   Uses tailor-made prompts to ensure summaries are systematic, detailed, and relevant to analytic philosophy.

4. **Cohesive Synthesis:**
   For extensive articles, combines summaries of different sections to deliver a cohesive and encompassing final summary.

5. **Adaptable Prompts:**
   Employs customizable prompts to adapt summarization techniques for articles in different fields.

## Usage:
1. **Setup:**
   - Store the articles intended for summarization in the `./articles` directory.
   - Obtain the necessary API key from OpenAI and set it as an environment variable `OPENAI_API_KEY`.

2. **Run:**
   Execute the `phd-gpt.py` script in your Python3 environment. The generated summaries will be stored in the `./summaries` directory.

```bash
$ python3 phd-gpt.py
```

3. **Review Summaries:**
   Examine the synthesized summaries located in the `./summaries` directory, each summary being appropriately named after its source article.

## Code Overview:
- **Dependencies:**
  - PyPDF2: For processing PDF files.
  - openai: For leveraging OpenAI's API.

- **Functions:**
  - `procure_text(article_name: str) -> str`: Retrieves and returns text content from the specified PDF article.
  - `lentext(article: str) -> int`: Calculates and returns the word count of the provided article.
  - `summarize_article(article: str, prompt: str) -> str`: Generates a summary for the input article using the provided prompt and returns the summary text.
  - `summarize_long(article: str, article_name: str) -> str`: Oversees the summarization of extensive articles, orchestrating the chunking and final synthesis processes.
  - `main() -> None`: The principal function initiating the summarization process for each article in the specified directory.

- **Execution:**
  The script operates by processing each PDF file in the `./articles` directory and formulating summaries in the `./summaries` directory.

## Requirements:
- Python 3.x
- PyPDF2
- openai

## Installation:
```bash
$ pip3 install PyPDF2 openai
```

## Environment Variables:
- `OPENAI_API_KEY`: Essential for authenticating with the OpenAI API.

## Setting up the OPENAI_API_KEY:
To set up the `OPENAI_API_KEY`, you need to add it to your environment variables. Here's how you can do it:

### On Linux/Mac:
1. Open your terminal.
2. Open your shell profile file (usually `~/.bashrc`, `~/.bash_profile`, or `~/.zshrc`) with a text editor. For example:
   ```bash
   $ nano ~/.bashrc
   ```
3. Add the following line at the end of the file:
   ```bash
   export OPENAI_API_KEY='your_api_key_here'
   ```
4. Save and close the file.
5. Reload the profile file to apply the changes:
   ```bash
   $ source ~/.bashrc
   ```

### On Windows:
1. Open the Start Menu and search for “Environment Variables.”
2. Click on “Edit the system environment variables.”
3. In the System Properties window, click on “Environment Variables…”.
4. In the Environment Variables window, click on “New…” under the User variables section.
5. Enter `OPENAI_API_KEY` as the Variable name and your API key as the Variable value.
6. Click OK to close each window.

## Customizing Prompts for Different Fields:
To adapt the prompts for a field other than analytic philosophy, modify the `reg_prompt`, `chunk_prompt`, and `final_summary_prompt` strings in the `phd-gpt.py` script to suit the terminologies, intricacies, and emphasis needed for that particular field.

## Considerations:
- Proper configuration of the OpenAI API key is crucial; failure to do so will impede the summarization process.
- While the tool is optimized for analytic philosophy articles, modifying the prompts can adapt the tool to other domains, but the effectiveness may vary.

## Limitations:
- The summarization quality is dependent on the clarity and quality of the input article.
- It is developed to work optimally with well-structured PDFs and may encounter difficulties with poorly formatted or scanned PDFs.

## Contribution:
Contributions for refining and enhancing phdGPT are warmly welcomed. Feel free to open issues or create pull requests for improvements.

## License:
GPL-3.0 License

## Contact:
mst387@uky.edu
https://github.com/storozhenko98

# Para Translate

A terminal-based tool for translating documents using the Ollama API locally.

## Features

- List and select documents from a specified directory.
- Read and write `.docx` and plain text files.
- Segment text into paragraphs for easier translation.
- Translate text using the Ollama API with various models.
- Interactive terminal interface for language and model selection.
- Side-by-side view of source text and translations.

## Requirements
- Ollama installed.
- Python 3.x
- `curses` module (standard library on Unix-like systems)
- `python-docx` library
- `ollama` library
- A `languages.txt` file containing a list of languages.

## Installation

1. **Clone the Repository**

   ```sh
   git clone https://github.com/emincangencer/para-translate.git
   cd para-translate
   ```

2. **Install Dependencies**

   Make sure you have `pip` installed, then run:

   ```sh
   pip install -r requirements.txt
   ```

3. **Set Up Languages File**

   Edit a file named `languages.txt` in the same directory as the script to add the languages you want to use, one per line.

4. **Prepare Documents**

   Place your documents in a directory named `documents`. Supported file types are `.docx` and plain text.

## Usage

1. **Run the Script**

   Launch the script using:

   ```sh
   python3 translator.py
   ```

2. **Interactive Interface**

   - **Select Source Language:** Use the UP and DOWN arrow keys to choose the source language.
   - **Select Target Language:** Use the LEFT and RIGHT arrow keys to choose the target language.
   - **Select Document:** Use the UP and DOWN arrow keys to choose a document from the `documents` directory.
   - **Select Translation Model:** Use the UP and DOWN arrow keys to select a model. Press `Enter` to confirm, or `r` to refresh the model list.
   - **Translate Paragraphs:** Use the UP and DOWN arrow keys to navigate through paragraphs. Press `Enter` to translate the selected paragraph, or RIGHT arrow key to skip translation.
   - **Quit:** Press `q` to quit the application.
   - **Note:** In some places, double press to confirm might be necessary. E.g. `q` + `q`.

3. **Translations Directory**

   Translations will be saved in a directory named `translations` with filenames based on the original document and target language.

## File Structure

- `translation_tool.py` - The main script.
- `languages.txt` - List of supported languages.
- `documents/` - Directory containing the documents to be translated.
- `translations/` - Directory where translated documents will be saved.

## Troubleshooting

- **No Languages Found:** Ensure `languages.txt` exists and is correctly formatted.
- **Document Errors:** Check the `documents` directory for supported file types and correct filenames.

## TO DO
    - Better handling long paragraphs for LLM.
    - Translate headers and footers.
    - Transfer indents and spaces.
    - Transfer docx file formatting (Font etc.).
    - Better UI handling.
**Look into:**
    - Post editing.
    - More file formats.
    - More API to use for translation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Ollama API](https://ollama.com) for running LLM models locally.

---
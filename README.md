-----

# 📸 Image Text Extractor with Gemini Vision AI

-----

## 🌟 Project Description

This Python project leverages the power of **Google's Gemini Vision AI** to accurately extract text from a series of images and compiles it into a single, organized Microsoft Word document. Whether you're digitizing old documents, extracting information from screenshots, or processing a batch of images for data entry, this tool automates the tedious task of manual text transcription.

It's designed to be user-friendly and highly configurable, making it a valuable asset for researchers, students, developers, and anyone needing to quickly convert visual information into editable text.

## ✨ Features

  * **Batch Image Processing:** Easily process multiple images in a specified range.
  * **Gemini Vision AI Integration:** Utilizes Google's state-of-the-art AI for highly accurate text extraction.
  * **Secure API Key Handling:** Fetches your Gemini API key from environment variables, keeping it secure and out of your codebase.
  * **Configurable Image Naming:** Supports flexible image filename patterns (e.g., `image_0001.jpg`, `doc_0002.png`).
  * **Word Document Output:** Compiles all extracted text into a well-formatted `.docx` file, ready for editing or archiving.
  * **Robust Error Handling:** Includes basic error handling for missing files and API call issues.
  * **Rate Limit Management:** Incorporates a customizable time delay between API calls to prevent hitting service rate limits, ensuring smooth operation for large batches.

## 🚀 Getting Started

Follow these steps to get your Image Text Extractor up and running\!

### Prerequisites

Before you begin, ensure you have the following installed:

  * **Python 3.8+**
  * **Google Gemini API Key:** You'll need to obtain an API key from the [Google AI Studio](https://aistudio.google.com/app/apikey).
  * **Required Python Libraries** (listed in `requirements.txt`).

### Installation

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/chenming777/Extract-images-word.git
    cd Extract-images-word
    ```

2.  **Install the necessary Python libraries:**

    ```bash
    pip install -r requirements.txt
    ```

### Configuration

Open the `image_text_extractor.py` file and update the following variables in the **`--- Configuration ---`** section:

  * **`START_INDEX` & `END_INDEX`**: Define the numerical range of your image filenames. For example, if your images are `image_0001.png` to `image_0010.png`, set `START_INDEX = 1` and `END_INDEX = 10`.
  * **`FILE_PREFIX` & `FILE_SUFFIX`**: Specify the constant parts of your image filenames.
      * Example: For `document_0005.jpg`, `FILE_PREFIX = "document_"` and `FILE_SUFFIX = ".jpg"`.
  * **`IMAGE_DIRECTORY`**: Provide the absolute or relative path to the folder containing your images.
      * Example: `IMAGE_DIRECTORY = r"C:\Users\YourName\Documents\MyImages"` or `IMAGE_DIRECTORY = r"./my_images"`.
  * **`OUTPUT_WORD_FILE`**: Set the desired name and path for your output Word document.
      * Example: `OUTPUT_WORD_FILE = r"C:\Users\YourName\Extracted_Texts.docx"` or `OUTPUT_WORD_FILE = r"./extracted_content.docx"`.

### Setting Your Gemini API Key

This project securely loads your API key from an environment variable. **DO NOT hardcode your API key directly in the script for public use or version control.**

**How to set the `GEMINI_API_KEY` environment variable:**

  * **On Linux/macOS:**
    Open your terminal and add the following line to your `~/.bashrc`, `~/.zshrc`, or equivalent shell configuration file:

    ```bash
    export GEMINI_API_KEY="YOUR_GEMINI_API_KEY_HERE"
    ```

    After saving, run `source ~/.bashrc` (or your relevant file) to apply the changes.
    Alternatively, for a single session:

    ```bash
    export GEMINI_API_KEY="YOUR_GEMINI_API_KEY_HERE"
    ```

  * **On Windows (Command Prompt):**

    ```cmd
    set GEMINI_API_KEY="YOUR_GEMINI_API_KEY_HERE"
    ```

    For persistent setting, you can use the System Properties (Environment Variables) GUI.

  * **On Windows (PowerShell):**

    ```powershell
    $env:GEMINI_API_KEY="YOUR_GEMINI_API_KEY_HERE"
    ```

    For persistent setting, add it to your PowerShell profile or use the System Properties.

Replace `"YOUR_GEMINI_API_KEY_HERE"` with the actual API key you obtained from [Google AI Studio](https://aistudio.google.com/app/apikey).

## ⚙️ Usage

Once configured and your API key is set as an environment variable, run the script from your terminal:

```bash
python image_text_extractor.py
```

The script will:

1.  Iterate through your specified image files.
2.  Send each image to the Gemini Flash for text extraction.
3.  Print the extracted text to the console.
4.  Append the extracted text to a new paragraph in the specified Word document.
5.  Pause for 20 seconds between each image to avoid hitting API rate limits.
6.  Save the final Word document with all the extracted content.


## 🤝 Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. Don't forget to give the project a star\!

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

Distributed under the MIT License. See the `LICENSE` file for more information.

## 📧 Contact

Teh Chen Ming - tehchenming7777@gmail.com

Project Link: https://github.com/chenming7777/Extract-images-word

-----

## **Happy Text Extracting\!**

### Action Items for You:

1.  **Create `requirements.txt`:** If you haven't already, create this file in your project's root with the content provided.
2.  **Create `LICENSE` file:** Choose an open-source license (MIT is simple and common) and create a `LICENSE` file in your project's root. You can find templates online.
3.  **Optional: Add a screenshot/GIF:** A visual example of your script's output or its operation significantly enhances the README.
4.  **Update Contact Info:** If you want, fill in your actual email or a link to your preferred contact method.

This `README.md` is comprehensive and highlights the secure API key handling, which is a great selling point for an open-source project\!

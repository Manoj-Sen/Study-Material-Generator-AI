# README

## Files Included

- `image.py`: This file contains code to retrieve the most relevant image using the Google Custom Search API.
- `study_material.py`: This file involves generating a study material using the OpenAI GPT-3.5 Turbo model. It creates a study material in JSON format and then converts it into a PDF.
- `lang.py`: This file integrates the Langchain library to perform language translation using the GPT-3.5 Turbo model.
- `pdf.py`: This file is responsible for creating a PDF document based on the generated JSON data from the `study_material.py` file.

## File Descriptions

### `image.py`

This script uses the Google Custom Search API to find the most relevant images based on a search query. It then extracts the image URLs from the API response.

### `study_material.py`

This script generates a study material using the OpenAI GPT-3.5 Turbo model. It prompts the model to create a JSON representation of the study material with various sections and content points. It also retrieves and embeds images into the JSON data. Finally, it converts the JSON data into a PDF document.

### `lang.py`

This script integrates the Langchain library to perform language translation using the GPT-3.5 Turbo model. It translates the JSON data generated by the `study_material.py` script into the desired language.this code is for integrated the langchain for translation but unfortunately due to encoding issues not done yet due to lack of time although i have tried with number of prompts but othe language text contains some encodings that not supports the 'latin-1 encoding like hindi and others

### `pdf.py`

This script creates a PDF document based on the JSON data generated by the `study_material.py` script. It uses the FPDF library to generate the PDF and embed images from the internet. It also handles the removal of temporary image files.

## Instructions

1. Run the `image.py` script to retrieve relevant images using the Google Custom Search API. Make sure to provide the necessary API key and custom search engine ID.
2. Run the `study_material.py` script to generate a study material in JSON format. You can specify the study topic and content points.
3. If needed, you can use the `lang.py` script to translate the generated JSON data into a different language.
4. Finally, run the `pdf.py` script to convert the JSON data into a PDF document. The PDF will include the study material content along with embedded images.

## Dependencies

- Python
- OpenAI GPT-3.5 Turbo
- FPDF
- Langchain
- PIL (Python Imaging Library)
- Requests
## Usage

1. Install the required dependencies:
   - `pip install fpdf requests pillow langchain langchain-ai`

2. Replace the placeholders in `lang.py` with the appropriate API keys for LangChain and Google Custom Search API.

3. To generate study materials and PDFs:

   - Run `study_material.py`:
     - Provide a topic/title for the study material.
     - Define a list of points for the study material.
     - The script will generate a JSON study material and a corresponding PDF file.

4. To translate the generated study materials:

   - Modify the `lang.py` file to include your LangChain API key.
   - Uncomment and modify the relevant sections in `study_material.py` to include translation.
   - Run `study_material.py` again to generate translated JSON materials and PDFs.

5. JSON Files:
   - The generated JSON study materials are saved in the `json_files` directory.

6. PDF Files:
   - The generated PDF study materials are saved in the `pdf_files` directory.

## Test Files

- JSON study materials for testing purposes are located in the `json_files` directory.
- Corresponding PDFs generated from these JSON files are located in the `pdf_files` directory.

Feel free to explore, modify, and extend the scripts to suit your specific use case and requirements.
Obtain API Key:
## Getting Start with Custom Search Engine
 ### Visit the Google Cloud Console.
 - Create a new project or select an existing one.
 - Navigate to the "APIs & Services" > "Credentials" section.
 - Click "Create Credentials" and select "API Key."
The generated API key will be displayed. Be sure to secure it and restrict its usage appropriately.
Create Custom Search Engine:

### Go to the Google Custom Search page.
- Click on the "Get started" button to create a custom search engine.
- Follow the prompts to configure your search engine. Specify that you want it to search for images only.
- Complete the setup process to obtain a custom search engine ID (also known as the cx parameter).
- Configure and Use the API:

In your API request, use the API key you obtained and the custom search engine ID (cx) to make requests to the Google Custom Search JSON API.
## Notes
- Langchain not implemented just successfully created the json data unable to encode in the pdf
- Make sure to replace placeholder API keys, IDs, and other variables with your actual credentials before running the scripts.
- The scripts are meant to be executed in order, as they build upon each other's outputs.
- The scripts assume an internet connection is available for retrieving images and translation.

## 2.O UPDATE
- In the Directory of 2.O Study Material Generation the Notes from the custom features are added.
- if yu want to try you can use your google cloud credentials in it and can see the demo on the local gradio server.
- Right now only three classes and few subjects are added in it.
- you will have to use your own google and openAI credentials.
- In 2.O the feature of images addition from google custom search is not added yet.

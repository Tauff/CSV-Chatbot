# CSV Question Answering with Google Gemini API

This project allows users to load a CSV file and ask questions about its data. Using the Google Gemini API, it generates responses based on the CSV data content. The setup ensures the API key remains secure by storing it in an environment variable.

## Features
- Load and view CSV data.
- Ask questions related to the content of the CSV file.
- Generates answers based on the context of the data using Google Gemini API.

## Requirements

- Python 3.7+
- Necessary libraries in `requirements.txt`

## Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables
Create a `.env` file by copying from `.env.example`:
```bash
cp .env.example .env
```
In the `.env` file, replace `your_actual_api_key_here` with your actual Google Gemini API key:
```plaintext
GEMINI_API_KEY=your_actual_api_key_here
```

### 4. Prepare a CSV File
Ensure you have a CSV file ready to load. For testing purposes, you can create a simple one or use `sample_data.csv` if provided.

## Usage

Run the script to start interacting with the CSV data:

```bash
python main_script.py
```

1. When prompted, enter the path to your CSV file.
2. After the CSV is loaded, ask questions about the data, and the AI will generate responses.
3. Type `exit` to end the session.

## Example Interaction

```plaintext
Enter the path to your CSV file: path/to/yourfile.csv
CSV file loaded successfully.

You can now ask questions about the CSV data.
Ask a question (or type 'exit' to quit): What is the average value in column A?
Answer:
The average value in column A is 45.3.

Ask a question (or type 'exit' to quit): What are the top 5 categories in column B?
Answer:
The top 5 categories in column B are ...
```

## File Structure

```plaintext
my-project/
├── .gitignore
├── README.md
├── requirements.txt
├── .env.example
├── main_script.py
└── sample_data.csv       # Optional sample CSV for testing
```

## Notes
- Ensure your `.env` file is included in `.gitignore` to keep your API key private.
- The number of rows in the CSV that the model can process is limited for better performance.

## License

[MIT License](LICENSE)

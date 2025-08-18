# CodHelp Smart Assistant for Research Summarization

## Overview
This is an AI-powered assistant that helps users deeply understand and interact with large documents such as research papers, reports, or technical manuals.  
It supports PDF, TXT, Word, PPT, Excel, and JSON uploads, generates concise summaries, answers free-form questions, and poses logic-based challenges for comprehension and reasoning.

**Built by:** Vikas Singh

## Features
- **Document Upload:** Supports PDF, TXT, Word, PPT, Excel, and JSON files.
- **Auto Summary:** Generates a concise summary (≤150 words) immediately after upload.
- **Ask Anything:** Ask free-form questions about the document and get contextual answers with justifications.
- **Challenge Me:** The assistant generates three logic-based questions, evaluates your answers, and provides feedback with references to the document.
- **Contextual Understanding:** All answers are grounded in the uploaded document, with highlighted supporting snippets.
- **Model Selection:** Choose which Gemini model to use for answering questions (sidebar dropdown).
- **Instructions Sidebar:** Step-by-step usage instructions are always available.
- **Statistics & Accuracy:** View a bar graph of uploaded file types and assistant accuracy per file type.

## How to Run

1. **Install dependencies**  
   Make sure you have Python 3.8+ installed.  
   Install required packages:
   ```
   pip install streamlit PyPDF2 python-docx python-pptx pandas google-generativeai nltk python-dotenv
   ```

2. **Set up API Key**  
   - Create a `.env` file in the project directory.
   - Add your Google Gemini API key:
     ```
     GOOGLE_API_KEY=your_google_gemini_api_key
     ```

3. **Run the app**  
   Open a terminal in the project directory and run:
   ```
   streamlit run SmartAssistantUI.py
   ```

4. **Use the app**  
   - Upload a PDF, TXT, Word, PPT, Excel, or JSON file using the sidebar.
   - Select your preferred Gemini model in the sidebar.
   - View the auto summary.
   - Choose "Ask Anything" or "Challenge Me" to interact with the assistant.
   - See a bar graph of file upload statistics and assistant accuracy.

## File Structure

- `SmartAssistantUI.py` — Main Streamlit app.
- `.env` — Contains your API key.
- `README.md` — This file.
- `SmartAssistant.ipynb` — Architecture and workflow notebook (not required for running the app).

## Notes

- If you hit Gemini quota limits, wait for quota reset or switch to a different Gemini model.
- All answers and feedback are based strictly on the uploaded document.
- If you see "missing ScriptRunContext!" warnings, you can ignore them.
- For best results, use a paid API key or monitor your quota usage.
- **New:** The app now tracks which file types are uploaded most and shows assistant accuracy per file type in a bar graph.

---
**Demo:**  
To see a walkthrough, run the app and follow the sidebar instructions.

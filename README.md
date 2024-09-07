# Gemini PDF Chatbot

Gemini PDF Chatbot is a Streamlit-powered application that enables users to interact with an AI chatbot trained on content extracted from uploaded PDF files. The bot can answer questions based on the context within the documents provided by the user.

## Features

- **PDF Upload:** Allows users to upload and process multiple PDF files.
- **Text Extraction:** Efficiently extracts text content from the uploaded documents.
- **Conversational AI:** Leverages the Gemini AI model to respond to queries based on the extracted information.
- **Interactive Chat Interface:** A user-friendly interface for seamless communication with the chatbot.

## Getting Started

To run the application using Docker, follow these steps:

1. **Set Up Google API Key:**
   - Obtain a Google API key and add it to the `.env` file in the following format:

   ```bash
   GOOGLE_API_KEY=your_api_key_here
   ```

2. **Run the Application:**

   ```bash
   docker compose up --build
   ```

Once the setup is complete, the application will be accessible at <http://localhost:8501>.

### Cloud Deployment

To deploy the application to the cloud:

1. Build the Docker image:

   ```bash
   docker build -t myapp .
   ```

   If your cloud provider uses a different architecture (e.g., amd64), build the image for the correct platform:

   ```bash
   docker build --platform=linux/amd64 -t myapp .
   ```

2. Push the image to your Docker registry:

   ```bash
   docker push myregistry.com/myapp
   ```

Refer to Docker's [getting started guide](https://docs.docker.com/go/get-started-sharing/) for further details on building and pushing images.

### Local Development

Follow these steps to set up the project locally:

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/gemini-pdf-chatbot.git
   ```

2. **Install Dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Set Up Google API Key:**
   Add your Google API key to the `.env` file as described earlier.

4. **Run the Application:**

   ```bash
   streamlit run main.py
   ```

5. **Upload PDFs and Start Chatting:**
   - Upload PDF files via the sidebar.
   - Click "Submit & Process" to extract text and start chatting with the AI.

## Project Structure

- `app.py`: Main application script.
- `.env`: Environment variables, including the Google API key.
- `requirements.txt`: Lists the Python packages needed.
- `README.md`: Project documentation.

## Dependencies

- PyPDF2
- langchain
- Streamlit
- google.generativeai
- dotenv

## Acknowledgments

- [Google Gemini](https://ai.google.com/): For the underlying AI language model.
- [Streamlit](https://streamlit.io/): For the application interface framework.

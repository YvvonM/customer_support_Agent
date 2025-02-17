# Customer Support Assistant

## Overview
The **Customer Support Assistant** is a chatbot built using **Gradio** and **LangGraph** that categorizes customer queries, analyzes sentiment, and provides appropriate responses. It leverages the **Groq LLM** to generate responses based on categorized queries. If a query is negative, it escalates the issue to a human agent.

## Features
- **Automatic Categorization**: Classifies queries into Technical, Billing, or General categories.
- **Sentiment Analysis**: Determines whether the sentiment of a query is Positive, Neutral, or Negative.
- **Automated Responses**: Provides responses based on the query category.
- **Escalation Handling**: Automatically escalates negative sentiment queries to a human agent.
- **Interactive UI**: Uses **Gradio** for an easy-to-use web interface.

## Technologies Used
- **Python**
- **LangGraph** (for workflow management)
- **Langchain**
- **Groq API** (LLM model)
- **Gradio** (for UI)
- **dotenv** (for environment variable management)

## Installation

### Prerequisites
Ensure you have Python installed (>=3.8). You also need to have a **Groq API Key**.

### Steps
1. Clone this repository:
    ```sh
    git clone https://github.com/yourusername/customer-support-assistant.git
    cd customer-support-assistant
    ```
2. Create a virtual environment and activate it:
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate
    ```
3. Install dependencies:
    ```sh
    pip install -r requirements.txt
    ```
4. Create a `.env` file and add your **Groq API Key**:
    ```sh
    echo "GROQ_API_KEY=your_api_key_here" > .env
    ```

## Usage
Run the application using the following command:
```sh
python app.py
```
This will launch the Gradio interface, where you can enter queries and get responses.

## How It Works
1. **User submits a query** → Categorization (Technical, Billing, General)
2. **Sentiment Analysis** → Determines Positive, Neutral, or Negative sentiment
3. **Routing**:
   - If **Negative** → Escalated to a human agent
   - If **Technical** → Responds with a technical solution
   - If **Billing** → Provides billing-related assistance
   - If **General** → Answers general inquiries

## Example Query & Response
**Query:** "I can't log into my account."

**Response:**
```
Category: Technical
Sentiment: Neutral
Response: Please try resetting your password or contact support for further assistance.
```

## Contributing
If you'd like to contribute:
- Fork the repository
- Create a new branch (`git checkout -b feature-branch`)
- Commit your changes (`git commit -m 'Add new feature'`)
- Push to the branch (`git push origin feature-branch`)
- Open a Pull Request

## License
This project is licensed under the **MIT License**.

## Contact
For issues or suggestions, feel free to reach out!

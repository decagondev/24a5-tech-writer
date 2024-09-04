# Technical Writer Agent

## Introduction
This project demonstrates the development of a **Technical Writer Agent** designed to enhance developer productivity. By leveraging Retrieval-Augmented Generation (RAG), our agent dynamically updates and refines technical documentation, ensuring it remains accurate, up-to-date, and contextually relevant.

## Prerequisites
- Docker (for containerized usage)
- Python 3.11 (for local setup)
- GitHub account
- OpenAI API key

## Setup

### 1. Environment Variables:
Copy the sample environment file and edit it with your API keys:
```
cp .env.sample .env
```
Edit the `.env` file and add your required variables:
```
GITHUB_TOKEN=your_github_token
OPENAI_API_KEY=your_openai_key
REPO_PATH=your_repo_path
PR_NUMBER=your_pr_number
```

### 2. Docker Setup:
1. Build the Docker image:
   ```
   docker build -t technical-writer-agent .
   ```
2. Run the container:
   ```
   docker run --env-file .env technical-writer-agent
   ```

### Local Setup (Alternative to Docker):
1. Ensure you have Python 3.11+ installed.
2. Set up a virtual environment:
   ```
   python3 -m venv .venv
   source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
   ```
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Run the main script:
   ```
   python main.py
   ```

## Project Structure
- `main.py`: Main script that orchestrates the Technical Writer Agent
- `utility.py`: Contains utility functions for GitHub interactions and OpenAI API calls
- `requirements.txt`: List of Python dependencies
- `Dockerfile`: Instructions for building the Docker image
- `README.md`: Project documentation (this file)

## Now It's Your Turn!
We encourage you to personalize this project and address challenges in your own environment. Here's how you can get started:

### Minimum Requirements
1. **RAG Integration:** Implement Retrieval-Augmented Generation to enable your agent to access and utilize external information.
2. **Vector Database Implementation:** Create and implement a vector data store for efficient document embedding and retrieval.

### Stretch Goals
1. **Enhanced UI/UX:** Develop a user-friendly interface with features like real-time suggestions and auto-completion.
2. **Automated Content Updates:** Implement periodic checks and updates to keep documentation current.
3. **Integration with Existing Tools:** Develop integrations with common development tools (e.g., Confluence, Jira, Notion).
4. **Custom Features:** Add unique features that simplify your daily routines and improve efficiency.

## Privacy and Submission Guidelines
- **Submission Requirements:** Submit a link to your public repo or a Loom video showcasing your work on the [BloomTech AI Platform](https://app.bloomtech.com).
- **Sensitive Information:** If your implementation involves sensitive data, a detailed Loom video demonstration is acceptable instead of a public repository.

## Troubleshooting
- Ensure all required environment variables are set in your `.env` file.
- For Docker issues, check your Docker installation and version.
- If you encounter package issues in local setup, try updating pip: `pip install --upgrade pip`

## Need Help?
Refer to the project documentation or reach out to the course instructor or learning assistant.
# movie_bot

## Overview

`movie_bot` is a chatbot application designed to provide information about movies. It leverages a combination of Streamlit for the user interface, OpenAI for language processing, and Neo4j for graph-based data storage and retrieval.

## Prerequisites

Before running the application, ensure you have the following installed:

- Python 3.8 or higher
- pip (Python package manager)
- Neo4j database

## Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/sobebarali/movie_bot.git
   cd movie_bot   ```

2. **Install Dependencies**

   Use the following command to install the required Python packages:
   ```bash
   pip install -r requirements.txt   ```

3. **Set Up Environment Variables**

   Create a `.env` file in the root directory and add your OpenAI and Neo4j credentials:
   ```
   OPENAI_API_KEY=your_openai_api_key
   OPENAI_MODEL=your_openai_model
   NEO4J_URI=your_neo4j_uri
   NEO4J_USERNAME=your_neo4j_username
   NEO4J_PASSWORD=your_neo4j_password   ```

4. **Configure Streamlit Secrets**

   Add your OpenAI and Neo4j credentials to the Streamlit secrets file `.streamlit/secrets.toml`:
   ```toml
   [OPENAI]
   API_KEY = "your_openai_api_key"
   MODEL = "your_openai_model"

   [NEO4J]
   URI = "your_neo4j_uri"
   USERNAME = "your_neo4j_username"
   PASSWORD = "your_neo4j_password"   ```

## Running the Application

To start the application, run the following command:

```bash
streamlit run bot.py
```

This will launch the Streamlit app in your default web browser.

## Usage

- Interact with the chatbot by typing your questions in the input box.
- The bot can provide information about movies, actors, and directors using data from Neo4j.

## Code Structure

- `bot.py`: Main application file that sets up the Streamlit interface and handles user interactions.
- `agent.py`: Contains the logic for generating responses using the language model and Neo4j data.
- `llm.py`: Configures the language model using OpenAI's API.
- `graph.py`: Sets up the connection to the Neo4j database.
- `tools/cypher.py`: Handles Cypher queries for retrieving movie information.
- `tools/vector.py`: Manages vector-based retrieval of movie plots.
- `utils.py`: Utility functions for managing session state and messages.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any improvements or bug fixes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
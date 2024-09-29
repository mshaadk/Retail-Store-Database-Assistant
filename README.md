# Retail Store Database Assistant
## Overview
The Retail Store Database Assistant is a Streamlit application designed to assist retail store managers and analysts in querying their database effortlessly. Users can input natural language questions, and the app translates them into SQL queries to fetch relevant data from the store's inventory.

Powered by Langchain's semantic similarity model and Google Palm, this application ensures accurate and contextually relevant answers by fine-tuning queries based on previous examples (few-shot learning).

## Features
- **Natural Language Query**: Ask questions about your store's inventory, such as stock levels, revenue generation, or item discounts.
- **Automatic SQL Query Generation**: The app transforms questions into MySQL queries without manual intervention.
- **Few-Shot Learning**: Utilizes previously stored question-answer pairs to refine and improve the SQL query generation process.
- **Database Integration**: Connects to a MySQL database storing retail inventory data, retrieving real-time insights.

## How It Works
1. **User Input**: The user enters a question in the provided text input box.
2. **Few-Shot Learning**: The app matches the question against stored few-shot examples and generates an optimized SQL query.
3. **SQL Query Execution**: The query runs against the connected database, and the results are displayed to the user.
4. **Semantic Similarity Selector**: Uses the HuggingFace all-MiniLM-L6-v2 model to select relevant few-shot examples based on the user's question.

## Tech Stack
- **Frontend**: Streamlit for an intuitive UI.
- **Backend**: MySQL for database storage and Google Palm for NLP-driven query generation.
- **Langchain**: To handle SQL query generation and few-shot learning.
- **Chroma**: For semantic similarity vector storage.
- **HuggingFace Embeddings**: Used to encode the few-shot examples and compare them with user queries.

## Setup
### Prerequisites
1. Python 
2. MySQL Database
3. API key for Google Palm (Google Generative AI)
4. Docker (optional, for containerized deployment)

### Installation
1. Clone this repository:

```bash
git clone https://github.com/mshaadk/Retail-Store-Database-Assistant.git
cd Retail-Store-Database-Assistant
```

2. Install the required Python libraries:

```bash
pip install -r requirements.txt
```

3. Set up environment variables by creating a `.env` file in the root directory:

```env
GOOGLE_API_KEY=<your-google-api-key>
```

4. Set up your MySQL database:

Ensure you have the correct tables (t_shirts, discounts) and data for the queries to function.

5. Run the app:

```bash
streamlit run main.py
```

## Example Queries
"How many t-shirts do we have left for Nike in XS size and white color?"
"How much is the total price of the inventory for all S-size t-shirts?"
"If we have to sell all the Levi’s T-shirts today, how much revenue will our store generate (post discounts)?"

## Future Improvements
- Add support for multiple databases.
- Integrate other language models for enhanced performance.
- Extend few-shot learning capabilities with more dynamic example storage.

## Collaborations
We encourage contributions and collaborations. If you wish to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Submit a pull request with a clear description of your changes.
4. If you would like to collaborate on a larger feature, feel free to open an issue, and we can discuss it further.
   
If you're interested in partnering for extended development or have suggestions, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/mohamedshaad/) or open an issue in the repository.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.



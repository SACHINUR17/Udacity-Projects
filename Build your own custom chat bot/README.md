## LLM Custom Chat Bot with RAG

### Execution Instructions

1. **Create the necessary Conda environment (Python 3.9 recommended):**
   ```sh
   conda create --name chatbot python=3.9
   conda activate chatbot
   ```

2. **Clone the repository:**
   ```sh
   git clone <repository_url>
   cd <repository_directory>
   ```

3. **Install the required packages:**
   ```sh
   pip install -r requirements.txt
   ```

4. **Open the Jupyter notebook:**
   ```sh
   jupyter notebook project.ipynb
   ```

5. **Replace the API key:**
   Locate the line:
   ```python
   openai.api_key = "YOUR API KEY"
   ```
   Replace `"YOUR API KEY"` with your actual OpenAI API key.

6. **Execute the notebook cells:**
   Run the cells sequentially to see the results. If you want to customize the project for your own dataset, custom data processing will be required. Adjust the cells as needed to fit your specific data and requirements.

## Workflow

#### Data Source
`character_descriptions.csv` - This file contains character descriptions from theater, television, and film productions. Each row includes the name, description, medium, and setting of the character. All characters were invented by an OpenAI model.

#### Reasoning for Selection
The dataset chosen for this project is particularly suitable for several reasons. Firstly, the characters within this dataset are invented by an OpenAI model, ensuring that they are unique and unlikely to be pre-existing entities within the knowledge base of any large language model (LLM). Consequently, directly querying the LLM about these characters without additional context would be ineffective and inappropriate.

To address this, we will generate embeddings for the character descriptions, allowing us to retrieve relevant context based on the user’s query. This context will be incorporated into a custom prompt, enabling the LLM to provide more accurate and contextually relevant responses. By leveraging this method, we enhance the LLM's ability to handle inquiries about these specific, unique characters, ultimately improving the quality and relevance of the generated answers.

#### Data Wrangling

##### Full Descriptive Text
Combine the columns into a single descriptive paragraph for each character.

**Format:**
```
[Name] is a [Description]. This character appears in a [Medium] set in [Setting].
```
**Example:**
```
Emily is a young woman in her early 20s, an aspiring actress. This character appears in a play set in England.
```

#### Workflow
1. **Inspecting Non-customized Results of Available Characters**
   - Understand how the LLM responds to queries about the characters without additional context.

2. **Get the Embeddings for the Text Data**
   - Generate embeddings for each character description to facilitate context retrieval.

3. **Get Relevant Text for Custom Prompt**
   - Retrieve the most relevant character descriptions based on the user's query using cosine similarity.

4. **Custom Prompt Creation**
   - Combine the user's query with the retrieved context to form a custom prompt.

5. **Custom Prompt Answering**
   - Use the custom prompt to query the LLM for more accurate and contextually relevant responses.

6. **Custom Performance Demonstration**
   - Demonstrate the improved performance of the LLM with the custom chatbot using specific queries about the characters.

By following this workflow, we ensure that the LLM can provide detailed and accurate answers about the characters in the dataset, leveraging the unique context provided by the custom prompts.

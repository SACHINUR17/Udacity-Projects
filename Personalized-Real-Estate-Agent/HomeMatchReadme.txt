# Personalized Real Estate Agent (HomeMatch) Notebook

## Overview

This notebook demonstrates the HomeMatch application, which matches users with suitable homes based on their preferences. It covers synthetic data generation, semantic search, and augmented response generation.

## Functionality

### Synthetic Data Generation
- Generating Real Estate Listings with an LLM: Uses a Large Language Model (LLM) to generate at least 10 diverse and realistic real estate listings.

### Semantic Search
- Creating a Vector Database and Storing Listings: Shows the creation of a vector database and storing real estate listing embeddings.
- Semantic Search of Listings Based on Buyer Preferences: Searches listings based on buyer preferences, returning matches that closely align with input preferences.

### Augmented Response Generation
- Logic for Searching and Augmenting Listing Descriptions: Uses buyer preferences to search and personalize real estate listing descriptions.
- Use of LLM for Generating Personalized Descriptions: Generates unique, appealing descriptions tailored to buyer preferences.

## Running the Code

1. Create and activate the conda environment:
    conda create --name agent python=3.10.11
    conda activate agent

2. Install the required packages:
    pip install -r requirements.txt

3. Launch the notebook:
    jupyter notebook HomeMatch.ipynb

## API Key Replacement

Replace the placeholder API key with your actual key in the notebook:

API_KEY = 'your_actual_api_key_here'

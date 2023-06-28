# ChatGPT-Translation

There are two datasets :

- World news data (in english)

- Book data (in mauritian creole)

The world news data contains data in english (source) and that has to be translated in mauritian creole (target).The code is available in the World news data folder that does the process.

The book data contains data in mauritian creole sentence(source) and that has to be translated in english (target).The code is available in the book translate folder that does the process.

## Overview

1. Import the required libraries (`openai`, `time`, and `csv`).
2. Set up the OpenAI API key.
3. Define the `translate_batch` function, which takes a batch of English sentences and returns their translations in Mauritian Creole.
   - Construct a prompt using the given English sentences.
   - Send a request to the OpenAI API using the constructed prompt.
   - Parse the API response to extract the translated sentences.
4. Specify the input and output CSV file names.
5. Set up the CSV reader and writer.
6. Loop through the input CSV file and read English sentences.
   - Collect sentences in a batch until the batch size is reached.
   - Call the `translate_batch` function to translate the batch of sentences.
   - Write the translated sentences to the output CSV file.
   - Flush the output file buffer after writing each batch.
7. If there are any remaining sentences after the loop, translate and write them to the output CSV file.

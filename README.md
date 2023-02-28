# Fraud Detection with NLP
Data loading and preprocessing code for the paper titled '**Fraud Detection with NLP**', which demonstrates the use of natural language processing techniques to detect fraud in financial transactions.

## Dependencies
This code requires the following Python packages:

* pandas
* numpy
* sklearn
* ast
* tensorflow

These can be installed using pip or another package manager.

## Usage
To use this code, you will need to have the following files in your **working** directory:

* _Fraud Detection with Natural Language Processing.pkl_: a pickled Pandas DataFrame containing the credit card transaction data
* _vocab.csv_: a CSV file containing a list of action names and their corresponding IDs

Once these files are in place, you can run the code and generate several new columns in the DataFrame, including:

* Action time mean: the average time between actions in a transaction
* Action time std: the standard deviation of the time between actions
* log(amount): the natural logarithm of the transaction amount
* Transaction Type: a string indicating whether the transaction is fraudulent or not
* time_to_first_action: the time between the start of the transaction and the first action taken
* actions_str: a string containing the names of all actions taken in the transaction
* total_time_to_transaction: the total time elapsed from the start of the transaction to its completion

## Notes

* The code assumes that the actions column in the DataFrame is a list of lists, where each inner list contains a sequence of actions taken in a single transaction.
* The code also assumes that the times column in the DataFrame is a list of lists, where each inner list contains the timestamp (in milliseconds) of each action taken in a single transaction.

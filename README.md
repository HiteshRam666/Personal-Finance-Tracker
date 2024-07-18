# 💰 Personal Finance Tracker 💰

This Personal Finance Tracker is a command-line application that helps you track your income and expenses. The data is stored in a CSV file, and you can add transactions, view transactions within a date range, and visualize the data through plots.

## ✨ Features

- ➕ Add new transactions with date, amount, category, and description.
- 📅 View transactions within a specified date range along with a summary of total income, total expense, and net savings.
- 📈 Plot income and expenses over time for a visual representation of your financial activities.

## 🛠️ Requirements

- Python 3.x
- pandas
- matplotlib

## 📦 Installation

1. Clone the repository or download the script files.
2. Install the required Python packages using pip:
    ```sh
    pip install pandas matplotlib
    ```

## 🚀 Usage

1. Run the `main.py` script:
    ```sh
    python main.py
    ```

2. Follow the on-screen instructions to:
    - ➕ Add a new transaction.
    - 📅 View transactions and summary within a date range.
    - 🚪 Exit the application.

## 🔧 Functions and Classes

### `get_date(prompt, allow_default=False)`

Prompts the user to enter a date in `dd-mm-yyyy` format. If `allow_default` is `True`, the current date is returned if no input is provided. Handles invalid date formats by prompting the user again.

### `get_amount()`

Prompts the user to enter a non-negative, non-zero amount. Handles invalid inputs by prompting the user again.

### `get_category()`

Prompts the user to enter the category of the transaction ('I' for Income or 'E' for Expense). Handles invalid inputs by prompting the user again.

### `get_description()`

Prompts the user to enter a description for the transaction. This is optional.

### `CSV`

A class to handle CSV file operations:
- `initialize_csv()`: Initializes the CSV file with appropriate columns if it doesn't exist.
- `add_entry(date, amount, category, description)`: Adds a new transaction entry to the CSV file.
- `get_transactions(start_date, end_date)`: Retrieves transactions within the specified date range and prints a summary.

### `add()`

A function to add a new transaction by calling `get_date()`, `get_amount()`, `get_category()`, and `get_description()` functions, then adding the entry to the CSV file.

### `plot_transactions(df)`

A function to plot income and expenses over time using the provided DataFrame.

### `main()`

The main function of the script which presents a menu to the user to choose between adding a new transaction, viewing transactions within a date range, or exiting the application.

## 📋 Example

```sh
1. Add a new transaction
2. View transactions and summary within a date range
3. Exit
Enter your choice (1-3): 1
Enter the date of the transaction (dd-mm-yyyy) or enter for today's date: 15-07-2024
Enter the amount: 100
Enter the category ('I' for Income or 'E' for Expense): I
Enter a description (optional): Salary
Entry added successfully
```

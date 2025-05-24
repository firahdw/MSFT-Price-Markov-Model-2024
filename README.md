
# MSFT Price Markov Model Analysis

This quantitative modeling project uses a Markov model to analyze Microsoft's (MSFT) historical stock price data from March 1986 to April 2025, with a focus on the year 2024. The dataset includes key indicators like open, high, low, close, adjusted close, and trading volume. The analysis aims to predict stock price transitions and future movements based on past data, providing insights into MSFT's market behavior.

## Prerequisites

To run this project, you will need the following Python libraries:

*   pandas
*   numpy
*   matplotlib

You can install these dependencies using pip:

```bash
pip install pandas numpy matplotlib
```

## Files

1.  **MSFT_1986-03-13_2025-04-06.csv**: A CSV file containing the historical stock data for Microsoft from March 1986 to April 2025.
2.  **MSFT_price_markov.ipynb**: The Jupyter notebook where the data is processed and analyzed using a Markov model.

## Usage

1.  **Data Loading**: The project begins by loading the Microsoft stock data from the CSV file using pandas:

    ```python
    df = pd.read_csv('MSFT_1986-03-13_2025-04-06.csv')
    ```

2.  **Data Preprocessing**: The 'date' column is converted to a pandas datetime format, and the data is filtered for the year 2024:

    ```python
    df['date'] = pd.to_datetime(df['date'])
    df_filtered = df[(df['date'] >= '2023-12-31') & (df['date'] <= '2024-12-31')]
    ```

3.  **Markov Model Application**: You can apply a Markov model (or any other machine learning model) on the filtered data to predict future stock prices based on the historical sequence.

4.  **Visualization**: The notebook uses matplotlib to create visualizations that help in understanding the trends and behaviors of the stock data.

## Data Columns

*   **date**: The date of the stock data entry.
*   **open**: The opening price for the stock on that day.
*   **high**: The highest price for the stock on that day.
*   **low**: The lowest price for the stock on that day.
*   **close**: The closing price for the stock on that day.
*   **adj_close**: The adjusted closing price, which accounts for splits and dividends.
*   **volume**: The number of shares traded on that day.

## Data Source

The Microsoft (MSFT) stock price data used in this project was sourced from Kaggle, specifically from the dataset titled **"Complete Microsoft Stock Dataset (1986–2025)"** by Muhammad Atif Latif. This dataset provides daily historical stock prices for Microsoft from March 13, 1986, to April 6, 2025.

You can access and download the dataset here:

👉 [Complete Microsoft Stock Dataset (1986–2025)](https://www.kaggle.com/datasets/muhammadatiflatif/complete-microsoft-stock-dataset-19862025)

## Contributing

Feel free to fork this repository, create branches, and open pull requests to contribute to the project.

## License

This project is licensed under the MIT License.

# Technical analysis and reporting tools

Here you will find a small collection of scripts to perform technical analysis of trading data in python. Sample data is in the `data` directory.

## Calculate rolling returns for a period

The `02price30f.py` python script calculates the 30-day future returns (rus., "скользящая доходность за 30-дневный период") for a given financial security by analyzing daily closing prices from a CSV file. It processes the data to get the closing price for each day, then uses vectorized operations to calculate the percentage change in price over a 30-day period. The script outputs the original date (open date), the closing price on that date, the price 30 days later (close date), and the 30-day future return percentage, saving the results to a new CSV file.

## Input requirements

Input file requirements: input csv must contain hourly data, `timestamp`, `symbol` (ticker), `price` (price observed at the date and time in `timestamp` field). Input does not contain headers.

## Usage: 

`python 02price30f.py <real_price_input_data.csv> <output_30_days_roll.csv>`


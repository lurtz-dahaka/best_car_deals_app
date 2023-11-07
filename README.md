# Best car deals finder bot

<div align="center">
  <a href="https://github.com/lurtz-dahaka/best_car_deals_app">
    <img src="https://imgur.com/e0FxNDG.jpg" alt="Logo" height="500">
  </a>
</div>

best_car_deals_app is a data science project that automates the process of finding the best car advertisements on Nettiauto.com, predicting car prices for new ads, and distributing the results using a Telegram bot.
The bot lives [HERE](https://t.me/Best_car_deals_bot).

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Data Sources](#data_sources)
- [Project Structure](#project_structure)
- [Model Building](#model_building)
- [Telegram Bot](#telegram_bot)
- [Technologies Used](#tech)
- [Contributing](#contributing)


## Overview <a name="overview"></a>

Application streamlines the process of finding car advertisements on Nettiauto.com, predicting car prices, and sharing the best ads with users through a Telegram bot. The project aims to assist users in identifying car deals that match their preferences and budget.

## Features <a name="features"></a>

- Web scraping Nettiauto.com using Selenium for car ads data.
- Feature engineering and data wrangling.
- Adding new data.
- Finding outliers and data cleaning.
- Building predictive models to estimate car prices.
- Identifying and presenting the best car advertisements.
- Deployment of app on Heroku.com
- Distributing results to users via a Telegram bot.

## Installation <a name="installation"></a>

1. Getting started 

```bash
# Clone the repository
git clone https://github.com/lurtz-dahaka/best_car_deals_app.git

# Navigate to the project directory
cd best_car_deals_app

# Install dependencies
pip install -r requirements.txt
```
2. Configure your project, including Nettiauto.com parsing settings and Telegram bot credentials.
3. Run the parser and wait until result.json is created:
```bash
python best_deals_collector.py
```
4. Run the bot:
```bash
python best_car_deals_bot.py
```

## Data Sources <a name="data_sources"></a>

- [Nettiauto.com](https://www.nettiauto.com): Car advertisements data source for web scraping.
- [Kaggle](https://www.kaggle.com/datasets/ander289386/cars-germany) dataset with used German cars characteristics.
- Finland cities population information obtained from Finland’s free-of-charge statistical [database](https://stat.fi/tup/tilastotietokannat/index.html).

## Project Structure <a name="project_structure"></a>

- data/: Data files and datasets.
- notebooks/: Jupyter notebooks for data analysis and model development.
- models/: Saved models for encoding, scaling and predicting.
- README.md: Project documentation.
- requirements.txt: Python dependencies.
- Procfile: declaring what commands are run by application's containers on Heroku platform
- .gitignore: ignoring files for committing to the GitHub repository
- .slugignore: causes files to be removed after you push code to Heroku and before the buildpack runs
- best_car_deals_bot.py: script for Telegram bot.
- best_deals_collector.py: script for parsing and collecting best offers.

## Model Building <a name="model_building"></a>

I used machine learning models (Linear Regression, Random Forest, XGBoost) to estimate car prices based on various features such as make, model, year, mileage, and more. Model development is detailed in Jupyter notebooks within the notebooks/ directory.

## Telegram Bot <a name="telegram_bot"></a>

best_car_deals_app uses a Telegram [bot](https://t.me/Best_car_deals_bot) to deliver results to users. Configure your Telegram bot credentials and customize the bot's behavior to suit your preferences.

## Technologies Used <a name="tech"></a>

- Python
- Pandas (dataframe management)
- RegEx (regular expressions)
- Scipy (statistical tests)
- Selenium (web scraping)
- Scikit-learn and XGBoost (machine learning)
- Joblib (pipelining)
- Aiogram (Telegram Bot API)
- Heroku CLI (deployment on Heroku)

## Contributing <a name="contributing"></a>

Contributions are welcome! Feel free to open issues, submit feature requests, or contribute code to enhance the project. 


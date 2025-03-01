## 🎬 Bollywood Dataset Project

### 📌 Description

This project contains an Excel dataset related to Bollywood movies, including attributes like movie names, release years, genres, actors, directors, box office collections, and more. It is useful for data analysis, visualization, and dashboard creation to gain insights into the Bollywood film industry.

### 📂 Dataset Details

📄 File Name: Bollywood Dataset.xlsx

📑 Format: Excel (.xlsx)

🔢 Number of Columns: Multiple attributes related to Bollywood movies.

📊 Key Columns:

🎥 Movie Name – Title of the Bollywood movie.

📅 Release Year – The year in which the movie was released.

🎭 Genre – The primary genre(s) (e.g., Action, Comedy, Drama, etc.).

🎬 Director(s) – Name(s) of the director(s).

🌟 Actor(s) – Leading actors.

💰 Box Office Collection – Revenue generated (in crores/millions).

⭐ IMDb Rating – User ratings from IMDb.

🎞 Production Budget – Cost incurred in producing the movie.

⏳ Duration – Movie length (in minutes).

🏳️ Language & Country – Language of the movie and country of production.

📝 Critic Score – Aggregate critic rating from various review platforms.

### 🎯 Objectives of Analysis

This dataset can be used for:
✅ Trend Analysis – Identify patterns in Bollywood over time.
✅ Revenue Insights – Study box office performance and its influencing factors.
✅ Top Performers – Find the most successful directors & actors.
✅ Budget vs Success – Does a higher budget lead to better revenue/ratings?
✅ Comparison Over Decades – Study how Bollywood evolved.
✅ Correlation Analysis – Understand relationships between different factors.

### 🚀 How to Use the Dataset

📌 Step 1: Clone the Repository
git clone https://github.com/yourusername/bollywood-dataset.git

📌 Step 2: Load the Dataset in Python

Use Pandas to read and analyze the dataset:

import pandas as pd
df = pd.read_excel("Bollywood Dataset.xlsx")
print(df.head())


📌 Step 3: Perform Data Cleaning

Check for missing values and clean the dataset:

print(df.isnull().sum())
df = df.dropna()  # Removing missing values if necessary

📌 Step 4: Exploratory Data Analysis (EDA)

Perform basic analysis and visualizations:

import matplotlib.pyplot as plt
import seaborn as sns

### Box Office Collection Distribution
plt.figure(figsize=(10,5))
sns.histplot(df['Box Office Collection'], bins=30, kde=True)
plt.title("Distribution of Box Office Collections")
plt.show()

--------------------------------------------------------------------------------------------

## 📊 Creating a Dashboard

A dashboard can be built using Plotly, Dash, or Power BI/Tableau.

🔹 Step 1: Using Plotly for Interactive Visuals

import plotly.express as px

fig = px.bar(df, x='Release Year', y='Box Office Collection', color='Genre', title='Box Office Collection Over Years')
fig.show()

🔹 Step 2: Using Dash for a Web-Based Dashboard

Dash can be used to build an interactive web-based dashboard.

📌 Install Dash:

- pip install dash

📌 Create an app file (app.py) and write the following code:

/* import dash
from dash import dcc, html
import plotly.express as px
import pandas as pd

df = pd.read_excel("Bollywood Dataset.xlsx")

app = dash.Dash(__name__)

app.layout = html.Div([
    html.H1("Bollywood Movies Dashboard"),
    dcc.Graph(
        figure=px.scatter(df, x='IMDb Rating', y='Box Office Collection', color='Genre', title='Rating vs Collection')
    )
])

if __name__ == '__main__':
    app.run_server(debug=True) */


📌 Run the app:

python app.py

### 🔧 Requirements

If you're working with the dataset in Python, install the necessary dependencies:

pip install pandas openpyxl matplotlib seaborn plotly dash


## 🤝 Contribution

You can contribute to this project by:

📌 Adding more data

📌 Improving data quality

📌 Performing new types of analysis

📌 Enhancing dashboard visuals

## 📜 License

This project is open-source. You can use, modify, and distribute it under the MIT License.

🚀 Happy Analyzing! 🎉


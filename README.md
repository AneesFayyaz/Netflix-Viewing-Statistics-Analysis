# Global Weekly Viewing Hours Analysis

This repository contains a comprehensive data analysis and visualization project focused on the global weekly viewing hours of various shows. Using Python libraries such as Pandas, Matplotlib, Seaborn, and Plotly, we explore and visualize the data to uncover trends and insights.


## Introduction

This project aims to analyze and visualize global weekly viewing hours data to uncover patterns and insights about the most popular shows and viewing habits across different categories and time periods.


## Requirements

To run this project, you'll need the following Python libraries:

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Plotly

You can install the required libraries using the following command:

```bash
pip install pandas numpy matplotlib seaborn plotly
```
## Analysis and Visualizations
**Category Distribution**
The first analysis involves understanding the distribution of categories in the dataset. We create a pie chart to visualize the proportion of different categories.
**Top 20 Most Viewed Shows**
We identify and list the top 20 most viewed shows based on weekly viewing hours.
```bash
top_20_most_viewed = df[['show_title', 'weekly_hours_viewed']].sort_values(by='weekly_hours_viewed', ascending=False).head(20)
print(top_20_most_viewed)
```
**Top 20 Most Viewed Shows (Combined Hours)**
We sum up the total viewing hours for each show and list the top 20 shows with the highest combined viewing hours.
```bash
combined_viewed_hours = df.groupby('show_title')['weekly_hours_viewed'].sum().reset_index()
top_20_most_viewed_combined = combined_viewed_hours.sort_values(by='weekly_hours_viewed', ascending=False).head(20)
print(top_20_most_viewed_combined)
```
**Category Viewing Hours**
We analyze the total viewing hours for each category and create a pie chart to visualize the data.
**Monthly Viewing Hours by Category**
![image](https://github.com/user-attachments/assets/bc607327-ff59-439a-a851-7688ae772a44)
**Scatter Plot**
![image](https://github.com/user-attachments/assets/56e4f7bd-286c-4ca5-8a49-ff685ec5ddb8)
**Heatmap**
![image](https://github.com/user-attachments/assets/7267eab0-9174-4b6c-976c-2bc4398f387f)



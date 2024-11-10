# Wellness-Insights-and-Activity-Metrics

Scenario:

A smart device used by individuals collects data on exercise, calories burned, total steps, exercise intensity, sleep, and more. The client has tasked us with analyzing this data to identify growth opportunities.

Goal:
Analyze the data to extract insights and identify trends and patterns in consumer behavior. With these insights, we can anticipate users' needs and tailor marketing strategies accordingly.

About the Data:

The data is sourced from fitness tracker bands of 33 unique individuals and contains personal fitness metrics.

We use 10 datasets:

  4 Daily Info files - merged into a single DataFrame.
  3 Hourly Info files - merged into a single DataFrame.
  Heart Rate, Weight Info, and Sleep Info - separate datasets.

Process:

Exploratory Data Analysis (EDA) and Data Cleaning

Using Python, we clean and prepare the datasets for analysis. Python's extensive library ecosystem makes data manipulation efficient, ensuring the data is in optimal condition before import into SQL Server.

Setting Up a Server:

We store and merge the data in SQL Server, which is ideal for handling and backing up data. SQL Server also supports data security through user authentication, role-based access, and encryption, ensuring data integrity.

Visualization:

Tableau converts raw data into dynamic, interactive visualizations. We connect Microsoft SQL Server to Tableau, allowing us to work with the latest data through scheduled refreshes if the data is continuously collected. Tableau's capabilities help create compelling data stories and allow seamless sharing across teams, departments, and clients.

View Dashboard on Tableau Public: https://public.tableau.com/app/profile/adnan.khan.pathan6792/viz/FitnessInfoDashboard/Dashboard2

Making Recommendations:

Based on our analysis, we will make recommendations to enhance user engagement, such as implementing alerts to keep users motivated, introducing activity challenges, and setting up a feedback system.
Conclusion

Our EDA process reveals that the Daily and Hourly datasets share similar IDs and Date/Day columns, allowing them to be merged in our database without issues. We cannot consolidate all data into a single table due to differing row counts across datasets and denormalization isn’t recommended. Using SQL Server we will merge data into two new tables in our schema, while other datasets are imported in their final form.

Tableau Dashboard: https://public.tableau.com/app/profile/adnan.khan.pathan6792/viz/FitnessInfoDashboard/Dashboard2

# Screen-Time-Analysis
This is a project that analyzes the screen time usage of a user on their  mobile device. 

# Prerequisites
<h3>To run this project, you will need the following:<br></h3>

Python 3.x<br>
Jupyter Notebook<br>
pandas library<br>
numpy library<br>
plotly library<br>

# Screen Time Analysis using Python 
 given some information about students like:<br>
 1.Date<br>
 2.Usage of Applications <br>
 3.Number of Notifications from Applications <br>
 4.Number of times apps opened<br>
 
 # Steps Involved
 <h3>Importing the necessary Python libraries and the dataset:</h3><br>
import pandas as pd<br>
import numpy as np<br>
import plotly.express as px<br>
import plotly.graph_objects as go<br>

data = pd.read_csv<br>
data.head()<br>

 <h3>Now let’s have a look if the dataset has any null values or not:</h3>
 data.isnull().sum()<br>
 
![image](https://github.com/Sanketarali/Screen-Time-Analysis/assets/110754364/b6f7a1f1-a0a9-4daf-a6e4-2c0a23ddd479)
 
 <h3>Now let’s start with analyzing the screen time of the user. I will first look at the amount of usage of the apps:</h3>
 figure=px.bar(data_frame=data,x='Date',y='Usage',title='Usage',color='App')<br>
figure.show()<br>

![image](https://github.com/Sanketarali/Screen-Time-Analysis/assets/110754364/71b42e0f-6a1a-4938-8d86-d0b4d9053ac9)

 <h3>Now let’s have a look at the number of notifications from the apps::</h3>
 figure=px.bar(data_frame=data,x='Date',y='Notifications',title='Notifications',color='App')<br>
figure.show()<br>

![image](https://github.com/Sanketarali/Screen-Time-Analysis/assets/110754364/0f6fa9b5-1683-4758-ad03-41ffd2a5d982)

 <h3>Now let’s have a look at the number of times the apps opened:</h3>
 figure=px.bar(data_frame=data,x='Date',y='Times opened',title='Notifications',color='App')<br>
 figure.show()<br>
 
![image](https://github.com/Sanketarali/Screen-Time-Analysis/assets/110754364/a4ef7e5e-bda8-44a5-bb91-8fe261181700)
 
 <h3>We generally use our smartphones when we get notified by any app. So let’s have a look at the relationship between the number of notifications and the amount of usage:</h3>
figure=px.scatter(data_frame=data,x='Notifications',y='Usage',trendline='ols',size='Notifications',title='Relationship Between Number of Notifications and Usage')<br>
figure.show()<br>

![image](https://github.com/Sanketarali/Screen-Time-Analysis/assets/110754364/ac7c8ad3-0b58-46e1-9c2e-fae3f8c6ad75)
 
 <h3>There’s a linear relationship between the number of notifications and the amount of usage. It means that more notifications result in more use of smartphones.</h3>




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
 1.Date 
 2.Usage of Applications 
 3.Number of Notifications from Applications 
 4.Number of times apps opened
 
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
 
 ![result](https://github.com/Sanketarali/Screen-Time-Analysis/blob/main/isnull.png)
 
 <h3>Now let’s start with analyzing the screen time of the user. I will first look at the amount of usage of the apps:</h3>
 figure=px.bar(data_frame=data,x='Date',y='Usage',title='Usage',color='App')<br>
figure.show()<br>

 ![result](https://github.com/Sanketarali/Screen-Time-Analysis/blob/main/1st.png)

 <h3>Now let’s have a look at the number of notifications from the apps::</h3>
 figure=px.bar(data_frame=data,x='Date',y='Notifications',title='Notifications',color='App')<br>
figure.show()<br>

 ![result](https://github.com/Sanketarali/Screen-Time-Analysis/blob/main/2nd.png)

 <h3>Now let’s have a look at the number of times the apps opened:</h3>
 figure=px.bar(data_frame=data,x='Date',y='Times opened',title='Notifications',color='App')<br>
 figure.show()<br>
 
  ![result](https://github.com/Sanketarali/Screen-Time-Analysis/blob/main/3rd.png)
 
 <h3>We generally use our smartphones when we get notified by any app. So let’s have a look at the relationship between the number of notifications and the amount of usage:</h3>
figure=px.scatter(data_frame=data,x='Notifications',y='Usage',trendline='ols',size='Notifications',title='Relationship Between Number of Notifications and Usage')<br>
figure.show()<br>

  ![result](https://github.com/Sanketarali/Screen-Time-Analysis/blob/main/4th.png)
 




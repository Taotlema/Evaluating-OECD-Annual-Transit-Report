# Evaluating-OECD-Annual-Transit-Report

Movement is a vital part of our daily lives. It defines how we get to work, meet others, and gain access to the things we need to thrive. The ability to move people and resources has always been essential to our survival. Even today, it remains a core mechanic of our quality of life and the functions of the economy. As technology has advanced, we have created several ways to facilitate movement - via vehicles and systems, which we might often think of first in relation to transit. The act of movement through different technology systems will be the focus of this project. Leveraging data mining techniques to better understand contemporary transit and its implications.

## Introduction

There is an ongoing global conversation about how we move people and goods, particularly as economies aim to remain competitive while also prioritizing sustainable growth. The challenge is that no single mode of transit—cars, trains, or ships—fully addresses the balance between efficiency, cost, and environmental impact. My project will evaluate which transit modes currently serve as the most effective in distributing critical economic elements and participants, while also identifying the shortcomings that may hinder future development. In short, I want to answer: **Which modes of transit are most effective today, and how might their limitations shape what comes next?**

This however is a rather complicated question to try and answer, and it will require a modular approach before any one could provide a defintive solution. So, as I begin my research, I will ask questions like the following:

1) Which modes of transit are most effective today in terms of "movement" volume and effeciency?
2) How did transit patterns evolve over the time period recorded in the OECD's report?
3) What modes of transit of good and people heavily dependent on?
4) How do different countries vary in their transit mode dependencies?

## Understanding the Data

To conduct this research we will be using the OECD's Annual Transit Report which provides information on transit modes, volumes, types, and operational stipulations related to moving both goods and people. This resource can be accessed here:

https://data-explorer.oecd.org/vis?lc=en&df[ds]=dsDisseminateFinalDMZ&df[id]=DSD_TRENDS%40DF_TRENDS&df[ag]=OECD.ITF&df[vs]=1.0&dq=.A.....&lom=LASTNPERIODS&lo=5&to[TIME_PERIOD]=false&vw=tb}}$

There are 6 seperate reports in this collectin provided by the OECD with their respective datasets. This project plans to make use of all of these sets and have been labeled within the code accordingly. Below are their descirptions: 

- **trends_data:** Comprehensive transit trends report using a combined measure of freight tonnes to kilometers, providing an overview of overall transportation activity across different modes.
- **freight_data:** Tracks all forms of cargo referred to as freight and its distribution across various transportation modes including road, rail, maritime, pipeline, and inland waterways.
- **container_data:** Dataset specifically tracking the movement of containers (standardized industrial metal boxes) for the movement of goods, particularly important for international trade and logistics.
- **passenger_data:** Dataset showing trends in the movement of passenger volume across different transit modes, focusing on how people move within and between regions.
- **incidents_data:** Dataset linked to safety reporting, focusing on total fatalities and injuries that have occurred.
- **length_data:** Shows the length of infrastructure implemented for different transportation modes, measuring the physical footprint of transportation networks.

Notably, these dataset carry information needed to evaluate each transit mode. If you would like to take a look at the fields of dataset, you can access the CSV files in this very repository. That said, I want to note what metrics I am specifically lookingt at:

- **Transport Mode**: The different methods of transportation (Roads, Rail, Inland Waterways, Pipelines, etc.)
- **Volume Measures:** Quantities of Frieght, Containers, or Passengers moved.
- **Temporal Data:** Information indicating the year of transit activies.
- **Country Data:** Details on where transit activities are occuring.
- **Infrastructure Metrics:** Length and capacity measures on transit networks.
- **Safety Metrics:** Incident, injury, and fatality data.

## Data Evaluations
Following my modular questioning plan to answer my greater question, I plan on launching several investigations. As of now, I have only completed the General Investigation meant to outline the basic trends and overview of transit activities. 

The first step of course is to process the data provided by the OECD, and then utilized specialized scirpts for each Investigation point.

### Preprocessing
The datasets used in the project have already been filtered by the OECD, however, I do run my own code to clean up these sets just to be on the safer side. Removing duplicates and Null records in the dataset to avoid these values from skewing the accuracy of my evaluations. While this is not technically cleaning, I do take the liberty to standardize the names of columns and created a combined database - however, I have yet to fully leverage this component in my investigation.

You might notice in my code that I do remove some of the recorded tranist catagories identified as {TOT_INL: Total Inland, HIRING - Third-Party Movers , OWN - Own transportation} since these were either aggreate or did not share much information on the means for transporatation.

### General Investigation

## Understanding the Results

### Conclusion and Takeaways

### Impact

## References
1) OECD International Transport Forum. (2024). Transport Statistics Database.
2) OECD. (2023). Annual Transport Trends Report. OECD International Transport Forum Publishing.
3) Python Software Foundation. (2023). Python 3.x. Retrieved from https://www.python.org/
4) McKinney, W. (2023). pandas: Python Data Analysis Library. Retrieved from https://pandas.pydata.org/
5) Hunter, J. D. (2007). Matplotlib: A 2D graphics environment. Computing in Science & Engineering, 9(3), 90-95.
6) Waskom, M. L. (2021). seaborn: statistical data visualization. Journal of Open Source Software, 6(60), 3021.

Generative AI-Models, specifically Claude Sonnet 4 was leveraged when learning to code or optimize scirpts for this project.

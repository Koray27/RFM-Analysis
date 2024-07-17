# RFM-Analysis
RFM Analysis in HR Department
Using RFM Analysis in the HR Department
While preparing a dashboard for the Sales Department, I noticed that among many metrics, one stands out as particularly crucial: RFM analysis. Every dashboard must include RFM analysis. I realized that this method is also suitable for the HR Department. If you are familiar with the 9-Box Grid, you know what I mean.
To effectively showcase our employees' performance, we need a reliable system. There are many systems for analyzing performance, and one of the best is the 9-Box Grid. It provides a fantastic visual representation, allowing you to analyze your employees' performance easily, quickly, and fairly. Let's dive into it step by step.
Typically, the 9-Box Grid shows us how many "Future Leaders" or "Under Performers" we have. However, it doesn't provide specific details such as names, departments, or other relevant information. The 9-Box Grid can show us what we need.
When you research the 9-Box Grid, you will find many similar tables. This is the work we are accustomed to;
 However, these tables often lack detailed information. In this article, I will show you how to add these details to our 9-Box Grid table. We will be conducting a more detailed and data-driven study than we are used to.
We need data that includes columns for names, performance, and potential. If you need more specific information, you can add it to your database.
This is our database;
Fist of all we will add a pivot table. Then we will need a measure in Power Pivot. This measure needs to include the table name and column name. The measure is:
Per-Pot=CONCATENATEX('Table';[Name];" - ";[Name];asc)
You can see the result in the picture.Every cell has a huge amount of words. We can't see where our workers are, our aim is to show string data to our customers or audience in the value field. If we achieve this, we will be able to see the performance and potential of our employees.
But we need a measure to see our data in the 9-Box Grid.
Creating a Pivot Table:
Drop the Per-Pot measure into the Value field. This will show our employees' names. However, we want to see their performance and potential scores together.
Therefore, we will drop the performance card into the rows and the potential card into the columns.

Using Slicers:
To separate the concatenated names, we will utilize slicers.
Since we cannot change the pivot table directly, we will show our pivot in a different sheet. For this, we will use GETPIVOTDATA, which will be useful to control our pivot. We will display them like this.

Creating an Additional Pivot Table:
Prepare a second pivot table without the Per-Pot measure.
Drop the ID card into the value field and choose "Distinct Count."

Displaying in 9-Box Grid:
HR managers prefer to work with percentage values, so we need to show both employee numbers and percentage values.
Display these values in a 9-Box Grid table. This way, when managers look at the table, they will see not only the employee's name and surname but also their performance-potential scores. They will also see how many people hold this card and what percentage of the department holds this card.
Then we will add a string value in our cards. We can see easily where our workers are and how many people there are We will show our data together. For instance, it will look like 17 ( 18,73%).

By following these steps, HR managers can see the performance and potential of employees both by name and in general percentage values. This provides a more data-driven and detailed analysis.

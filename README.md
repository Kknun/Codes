#1 Canada Immigration Set

import pandas as pd
import plotly.express as px

# Sample data
data = {
    'Date': ['2020-01', '2020-02', '2020-03', '2020-04', '2020-01', '2020-02'],
    'Program': ['FSW', 'CEC', 'FSW', 'PNP', 'CEC', 'FST'],
    'Invitations': [1500, 1200, 1800, 900, 1100, 800],
    'CRS_Score': [450, 470, 460, 480, 465, 455]
}
df = pd.DataFrame(data)

# a. Line plot
fig1 = px.line(df, x='Date', y='Invitations', title='Invitations Over Time', markers=True)
fig1.show()

# b. Bar chart
fig2 = px.bar(df, x='Program', y='Invitations', title='Total Invitations by Program')
fig2.show()

# c. Boxplot
fig3 = px.box(df, x='Program', y='CRS_Score', title='CRS Score Distribution by Program')
fig3.show()

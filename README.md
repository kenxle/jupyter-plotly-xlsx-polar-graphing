# Radial Graphing, from Excel to Jupyter

[See the medium article](https://medium.com/@kenstclair/radial-graphing-for-solution-evaluation-36c29050f250)


This solution allows you to record evaluative ratings and have them piped into radial graphs in a quick and easy way. 

# Installation
1. Download or clone the repo
2. [Edit Polarities.xlsx](https://github.com/kenxle/jupyter-plotly-xlsx-polar-graphing/blob/master/README.md#the-sheets)
3. Start Jupyter Notebook and open Radial Graphing.ipynb
4. Run each code block in order
5. Export images or screencap

# The Excel Sheets
The tab "Ratings" allows you to create the ratings for each of your criteria. The number of criteria is flexible and the graph will adjust automatically. Criteria names that are put on the first row will show up as labels in the graphs, and the names down the first column will be graph titles. Notes should always be in the final column, and will be added to individual graphs automatically. Line breaks need to be added in the text with HTML style: "<br />". 

The tab "Overlays" allows you specify which sets you want overlaid. Use the excel row number from sheet "Ratings" to specify overlays. You can overlay any number of graphs by continuing to add row numbers in the Overlays tab. Each row generates a new graph, each column adds a rating set to that row's set of overlays. 

# Settings
* By default, the excel file is named "Polarities.xlsx". If you'd like to change it, there's a variable `filename` in the first code block.
* By default, the excel file is in the same folder as the Jupyter Notebook file. You can change this using the variable `sdir` in the first code block. 
* By default, the sheets are named "Ratings" and "Overlays". The variables in the first code block named `sheet` allow you to control these.
* The rating ranges default from 0-10. To change these, find the variables `rating_lower_range` and `rating_upper_range` in the first code block. 
* By default, plotly operates in offline mode. If you'd like to enable uploads, remove the line `init_notebook_mode(connected=True) #use plotly offline`.

# table-visualization
Visualizes breast cancer data read from a table. 

based on the example found here: http://bl.ocks.org/mbostock/3213173

The data used is breast cancer data. It consists of data associated with individual patients.
There are ten traits of each patient that are recorded having to do with the characteristics of the cancer. 
This data can be useful for analyzing how different cancer characteristics interact with eachother. 

The data is for the most part already in an easy to work with form, but before it is charted, there are a few
alterations that must be made. There are some missing measurements, so those must be dealt with. Any unknown values
should be disregarded. The last column of the data represents whether or not the cancer was beneign or malignant. 
Those values are converted to strings representing the values. 

This visualization should work with more rows or more columns. There would just have to be one addition to the function
that reads the csv file. After that everything is built to deal with a dynamic data set. 

I based my code on the example listed above. I changed the color scheme so that patients with malignant cancer are 
represented as red and benign cancer patients are represented as blue. Since there are so many data points, I made 
each point partially transparent to show the difference between a space with ten data points on it and a space
with only one data point. I also added a feature that allows the user to select which columns to add to the 
scatterplot matrix. The user can select as many or as few as they want and the scatterplot matrix will resize. 

To make resizing the matrix easier, I made the function that draws it independent of the size. This way, I can externally
change the things that are selected to be drawn, and the actually drawing function will draw it all the same. 

To run the program, clone the repository and navigate to the top level. Run <code> python -m SimpleHTTPServer</code>
in the repository to serve the content. Open localhost:8000 in a browser to see the page. Click on the buttons to the
far right of the page to select which columns are visible. 
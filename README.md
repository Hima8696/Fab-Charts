# Fab-Charts
Fab Charts is an application which generates graphs for a given input dataset
Tab Charts is an application which generates graphs for a given input dataset. It’s a lightweight JavaScript application which preprocess the dataset using a parser and identifies the attributes present in dataset. We can isolate the attributes and plot the graph on required attributes.  The user can choose different type of graphs and can export them.

* Background :
Lot of chart libraries which are available on the web requires a basic knowledge of composing web pages and using scripting languages to use them. This programming knowledge prerequisite and understanding of libraries consumes a lot of time for visualizing the data, this impedes to enjoy the visualization of all available charts. So, we developed an application where use can draw graphs without writing any code, the user need not have programming knowledge or knowledge of any other libraries. They can generate graphs using one click and can save the graph as an image too.

* Design
Tab charts contains Five components where each component is dependent on other for generating the charts. The following figure shows the architectural implementation of TabCharts.

* Tab charts UI:
Tab Charts UI acts as a medium between the user and other components of Tab charts. In this, we input our data file for which we want to generate the charts. User provide different details for the graph generation namely, the Co-ordinates of the graph, type of charts, description of the graph axis.

* Tab Charts Preprocessor:
It contains a JavaScript parser which is responsible for reading the input data file and identifying the attributes of the data set. It reads each field of the given data set and makes the data ready for generating the graphs.

* Tab Charts Engine:
It’s the primary and core component of the Tab charts. Its responsible for generating the following components. They are:
•	Data Table
•	Options
It takes pre-processed data from the tab charts preprocessor component to generate the Data table and attributes, type of chart details from the Tab Charts UI component. These data components are appended to generated the google charts using the google charts library.

* Google Charts Library:
Google charts provides a rich library of graphs. We use visualization class of the google charts and input our data to generate our desired graph.

* Tab Charts Output:
After generating the chart using the other components the chart is displayed to the tab charts UI where user can export the chart as an image.


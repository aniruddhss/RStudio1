<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
   
</head>
<body>

<h1>Best-Selling Books on Amazon Dashboard</h1>

<p>This project is a <strong>flexdashboard</strong> that visualizes data on best-selling books from Amazon from 2009 to 2019. The dashboard provides interactive visualizations that highlight popular authors, books, and genres, and also lists the top-rated books by user ratings.</p>

<h2>Features</h2>

<p>The dashboard includes the following sections:</p>
<ul>
    <li><strong>Most Popular Authors:</strong> A column chart visualizing the 15 most popular authors based on the total number of reviews. Tooltips provide details about the number of reviews for each author when hovering over the chart.</li>
    <li><strong>Most Popular Books:</strong> A bar chart showing the top 15 most popular books based on the number of reviews.</li>
    <li><strong>Most Common Genre:</strong> A pie chart visualizing the proportion of books in different genres (e.g., Fiction and Non-Fiction).</li>
    <li><strong>Best Books by User Rating:</strong> A scrollable HTML table listing books with a user rating of 4.9 or higher, displaying the book title and author.</li>
</ul>

<h2>Installation</h2>

<p>To run this project, you need the following:</p>
<ol>
    <li>R (version 4.0 or higher)</li>
    <li>RStudio (recommended for ease of use)</li>
    <li>Install the necessary R libraries:</li>
</ol>

<div class="code">
install.packages(c("flexdashboard", "tidyverse", "highcharter", "gt", "htmltools", "viridis", "readr"))
</div>

<p>4. Clone or download this repository.</p>
<p>5. Ensure that the <strong>bestsellers with categories.csv</strong> file is in your working directory.</p>

<h2>Running the Dashboard</h2>

<p>To run the dashboard:</p>
<ol>
    <li>Open the <code>.Rmd</code> file in RStudio.</li>
    <li>Click the "Run Document" button or press <kbd>Ctrl + Shift + K</kbd> to generate the dashboard.</li>
    <li>The dashboard will be rendered in the RStudio viewer or your web browser.</li>
</ol>

<p>Alternatively, you can access a deployed version of the dashboard directly in your browser without any hassle:</p>
<p><a href="https://github.com/aniruddhss/RStudio1/blob/main/dashboard-books.html">Deployed Dashboard Link</a></p>

<h2>Data</h2>

<p>The dataset used in this project is <strong><a href="https://github.com/aniruddhss/RStudio1/blob/main/bestsellers%20with%20categories.csv">Bestsellers On Amazon</a></strong>, which includes the following columns:</p>
<ul>
    <li><strong>Name:</strong> The title of the book.</li>
    <li><strong>Author:</strong> The author of the book.</li>
    <li><strong>User Rating:</strong> The average user rating of the book (on a scale from 1 to 5).</li>
    <li><strong>Reviews:</strong> The total number of user reviews.</li>
    <li><strong>Price:</strong> The price of the book (in USD).</li>
    <li><strong>Year:</strong> The year the book was a bestseller.</li>
    <li><strong>Genre:</strong> The genre of the book (Fiction or Non-Fiction).</li>
</ul>

<h2>Code Explanation</h2>

<h3>Data Cleaning</h3>
<p>Duplicates based on the <code>Name</code> column are removed to ensure each book appears only once in the analysis.</p>

<div class="code">
df <- df %>% distinct(Name, .keep_all = TRUE)
</div>

<h3>Visualizations</h3>

<p><strong>1. Most Popular Authors:</strong> Grouped by <code>Author</code> and summarized based on the total number of reviews. Displayed in a column chart with a customized color palette using <code>hchart()</code> from the <code>highcharter</code> package.</p>

<p><strong>2. Most Popular Books:</strong> Books are sorted by the number of reviews and displayed in a bar chart.</p>

<p><strong>3. Most Common Genre:</strong> A pie chart showing the distribution of Fiction and Non-Fiction books based on the count of books in each genre.</p>


<p><strong>4. Best Books by User Rating:</strong> A scrollable HTML table showing the best books (User Rating >= 4.9), styled using the <code>gt</code> package for a polished look.</p>


<h2>Screenshots</h2>

<div class="screenshot">
    <img src="https://github.com/aniruddhss/RStudio1/blob/main/Screenshots/bestsellers_on_amazon_project_R_SS%20(1).png" >
    <img src="https://github.com/aniruddhss/RStudio1/blob/main/Screenshots/bestsellers_on_amazon_project_R_SS%20(2).png" > 
    <img src="https://github.com/aniruddhss/RStudio1/blob/main/Screenshots/bestsellers_on_amazon_project_R_SS%20(3).png" >
</div>


<h2>Credits</h2>
<p>This project was inspired by a tutorial from the <strong><a href="https://www.youtube.com/@datawithmiguel4900">DATA WITH MIGUEL</a></strong> YouTube channel. Special thanks for the guidance and inspiration!</p>
<p><a href="https://youtu.be/fkqD9kcvCkU?si=pikcUZV64KXw3Wy1" target="_blank">Watch the Tutorial</a></p>

<p class="credit">Developed by: <strong>AniruddhS</strong></p>

</body>
</html>

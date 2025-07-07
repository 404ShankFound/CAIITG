<h1>Dynamic Pricing for Urban Parking Lots – Project Walkthrough</h1>

<p>Capstone Project – Summer Analytics 2025<br>
Hosted by: Consulting & Analytics Club × Pathway</p>

<hr>

<h2>Project Overview</h2>
<p>In this project, I built a real-time dynamic pricing system for 14 urban parking lots using simulated streaming data. My objective was to adjust parking prices intelligently and smoothly based on live conditions like occupancy, traffic congestion, vehicle type, and more. The system was implemented from scratch using only pandas, numpy, pathway, and bokeh, as per the constraints.</p>

<hr>

<h2>Tech Stack Used</h2>
<table>
  <thead>
    <tr><th>Functionality</th><th>Technology</th></tr>
  </thead>
  <tbody>
    <tr><td>Data manipulation</td><td>pandas, numpy</td></tr>
    <tr><td>Real-time stream processing</td><td>Pathway</td></tr>
    <tr><td>Visualization</td><td>Bokeh</td></tr>
    <tr><td>Development environment</td><td>Google Colab</td></tr>
  </tbody>
</table>

<hr>

<h2>What I Did – Step-by-Step</h2>

<h3>1. Understanding the Dataset</h3>
<p>I began by exploring the provided dataset.csv which contained 18 time samples per day across 73 days for 14 parking locations. It included columns such as capacity, occupancy, vehicle type, queue length, traffic conditions, and a timestamp split into date and time fields.</p>

<h3>2. Data Cleaning and Preprocessing</h3>
<p>I cleaned column names and merged LastUpdatedDate and LastUpdatedTime into a single timestamp column using pd.to_datetime with dayfirst=true to handle the European-style date format. I then mapped vehicle types (car, bike, truck) to numerical weights for use in modeling.</p>

<h3>3. Building the Pricing Models</h3>
<p>I implemented two models:</p>
<ul>
  <li>Model 1: Baseline Linear – I created a simple linear pricing function that increased the price as a function of occupancy rate:</li>
</ul>
<pre><code>price[t+1] = price[t] + α * (occupancy / capacity)</code></pre>
<ul>
  <li>Model 2: Demand-Based Pricing – I constructed a demand function that combined multiple features:</li>
</ul>
<p>Occupancy rate, queue length, traffic congestion, special day flag, vehicle type weight</p>
<pre><code>price = base_price * (1 + λ * normalized_demand)</code></pre>
<p>I clipped the final price between 0.5× and 2× the base price to avoid erratic behavior.</p>

<h3>4. Pathway Integration</h3>
<p>Using Pathway, I created a streaming table from the DataFrame. I defined a schema using pw.Schema with DATE_TIME_NAIVE for timestamp fields. I then used pw.apply() to apply the pricing logic row-wise. I ensured the schema and input table matched perfectly to avoid type errors and mismatches.</p>

<h3>5. Real-Time Visualization with Bokeh</h3>
<p>To simulate real-time visual feedback, I used Bokeh’s ColumnDataSource and streaming updates to plot dynamic pricing curves over time. Since Colab has limited interactive support, I used push_notebook() and as_pandas() to plot prices on the fly in the notebook itself.</p>

<hr>

<h2>Architecture Diagram</h2>
<pre><code>graph TD
    A[Raw dataset.csv] --> B[Preprocessing in Pandas]
    B --> C[Stream as Pathway Table]
    C --> D[Apply Pricing Logic]
    D --> E[Dynamic Prices per Lot]
    E --> F[Bokeh Real-Time Plot]</code></pre>

<hr>

<h2>Project Files</h2>
<pre><code>.
├── dataset.csv                      # Input dataset
├── Note1book.ipynb                  # Final notebook
├── README.md             # This README file</code></pre>

<hr>

<h2>Submission Checklist</h2>
<ul>
  <li>Cleaned and transformed dataset</li>
  <li>Implemented Models 1 and 2</li>
  <li>Real-time simulation using Pathway</li>
  <li>Visualization with Bokeh</li>
  <li>Fully runnable notebook in Colab</li>
  <li>Markdown and PDF documentation</li>
</ul>

<hr>

<h2>Author</h2>
<pre>
Name - Shashank Nandan
Mail used to register for summer analytics - shashanknandan21@gmail.com
Manipal Institute Of Technology
</pre>

<hr>

<p>Thank you for your time and evaluation.</p>

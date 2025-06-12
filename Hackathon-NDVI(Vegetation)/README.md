<h1>🌿 Summer Analytics 2025: First Hackathon</h1>

<p>
  Welcome to the <strong>first course hackathon</strong> of <strong>Summer Analytics 2025</strong>,
  hosted by the <strong>Consulting & Analytics Club</strong> in collaboration with <strong>GeeksforGeeks (GFG)</strong>.
</p>

<p>
  Your challenge is to classify land cover types using <strong>NDVI time-series satellite data</strong> and <strong>OpenStreetMap (OSM)</strong> labels.
  Build a <strong>Logistic Regression</strong> model that accurately predicts land cover classes even with noisy data.
</p>

<p>
  🏆 <strong>Top performers</strong> win <strong>GFG Premium memberships</strong>, and all participants receive exclusive discounts.
</p>

<p>
  📺 <a href="https://www.youtube.com/watch?v=4BOtr1PZ2D8" target="_blank">Reference Video: How to Participate in Hackathons</a>
</p>

<hr/>

<h2>📝 Problem Statement: NDVI-based Land Cover Classification</h2>

<h3>📌 Key Concepts</h3>

<p><strong>NDVI (Normalized Difference Vegetation Index):</strong></p>

<pre>
NDVI = (NIR - Red) / (NIR + Red)
Where:
  NIR = Near-Infrared Reflectance
  Red = Red Reflectance
</pre>

<h3>⚠️ Data Challenges</h3>

<ul>
  <li><strong>Noise:</strong> Cloud cover and labeling inaccuracies.</li>
  <li><strong>Missing Data:</strong> Due to satellite obstruction (clouds).</li>
  <li><strong>Temporal Variation:</strong> Requires feature engineering for seasonal patterns.</li>
</ul>

<p><strong>Note:</strong> Training and public test data are noisy. Private leaderboard data is clean to evaluate generalization.</p>

<hr/>

<h2>📂 Dataset</h2>

<ul>
  <li><strong>ID:</strong> Unique sample identifier</li>
  <li><strong>class:</strong> Ground truth — one of:
    <code>{Water, Impervious, Farm, Forest, Grass, Orchard}</code>
  </li>
  <li><strong>27 NDVI Time Points:</strong> Columns like <code>20150720_N</code>, <code>20150602_N</code>, etc., representing NDVI values over time</li>
</ul>

<hr/>

<h2>📜 Rules</h2>

<ul>
  <li><strong>Model:</strong> Logistic Regression only (multiclass)</li>
  <li><strong>Preprocessing:</strong> Denoising, imputation, and feature engineering allowed</li>
  <li><strong>Leaderboard:</strong>
    <ul>
      <li><strong>Public (89%):</strong> Immediate feedback</li>
      <li><strong>Private (11%):</strong> Used for final evaluation</li>
    </ul>
  </li>
</ul>

<hr/>

<h2>🧮 Evaluation</h2>

<p><strong>Metric:</strong> Accuracy score</p>
<p><strong>Submission Format:</strong></p>

<pre>
ID,class
1,water
2,water
3,grass
4,impervious
...
</pre>

<hr/>

<h2>🏅 Leaderboard Highlights</h2>

<ul>
  <li><strong>Model-2:</strong> Public Score <code>0.78546</code> ✅ Best</li>
  <li><strong>Model-5:</strong> Runner-up</li>
  <li><strong>Model-3:</strong> Third place</li>
</ul>

<p><strong>Submissions:</strong> <code>SubmissionModel2.csv</code>, <code>SubmissionModel5.csv</code></p>

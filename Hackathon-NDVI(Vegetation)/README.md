<h1>Summer Analytics First Hackathon</h1>

<p>
  Welcome to First course hackathon of Summer Analytics 2025.
Hosted by Consulting & Analytics Club and GeeksforGeeks (GFG)
Classify land cover types using NDVI time-series data from satellite imagery and OpenStreetMap (OSM) labels. Your challenge is to build a Logistic Regression model that accurately predicts land cover classes despite noisy NDVI signals. Top performers win GFG Premium memberships, and all participants get exclusive discounts!
</p>

<p>
  <a href="https://www.youtube.com/watch?v=4BOtr1PZ2D8">Reference for Participating in Hackathons</a>
</p>

<h3>Description</h3>

<pre>
Hackathon Problem Statement: NDVI-based Land Cover Classification
Key Concepts

NDVI (Normalized Difference Vegetation Index)
Measures vegetation health using satellite data:
Where:-

NIR = Near-Infrared reflectance
Red = Red reflectance
2. Data Challenges
Noise: The main challenge with the dataset is that both the imagery and the crowdsourced data contain noise (due to cloud cover in the images and inaccurate labeling/digitizing of polygons).

Missing Data: Certain NDVI values are missing because of cloud cover obstructing the satellite view.

Temporal Variations: NDVI values vary seasonally, requiring careful feature engineering to extract meaningful trends.

Important Note:
The training and public leaderboard test data may contain noisy observations, while the private leaderboard data is clean and free of noise. This design helps evaluate how well your model generalizes beyond noisy training conditions.

<h3>Dataset</h3>
Each row in the dataset contains:

class: Ground truth label of the land cover type — one of {Water, Impervious, Farm, Forest, Grass, Orchard}

ID:Unique identifier for the sample

27 NDVI Time Points: Columns labeled in the format YYYYMMDD_N (e.g., 20150720_N, 20150602_N) represent NDVI values collected on different dates. These values form a time series representing vegetation dynamics for each location.

<h3>Rules</h3>
  
Model: Logistic Regression only (multiclass).

Preprocessing: Denoising, imputation, and feature engineering allowed.

Leaderboard:

Public (89% test data): Immediate feedback.

Private (11% test data): Final ranking (avoids overfitting).

<h3>Evaluation</h3>
Submissions will be evaluated on basis of accuracy score of the predicted class.

Submission format:
ID,class
1,water
2,water
3,grass
4,impervious
..
</pre>
<pre>
  <h1>Leaderboard</h1>
  Model-2 (Public Score:0.78546) had the best public score followed by Model-5 then by Model-3 of which submissions are SubmissionModel{2&5}
</pre>
📝 Problem Statement: NDVI-based Land Cover Classification
📌 Key Concepts
NDVI (Normalized Difference Vegetation Index):

𝑁
𝐷
𝑉
𝐼
=
(
𝑁
𝐼
𝑅
−
𝑅
𝑒
𝑑
)
(
𝑁
𝐼
𝑅
+
𝑅
𝑒
𝑑
)
NDVI= 
(NIR+Red)
(NIR−Red)
​
 
NIR = Near-Infrared Reflectance

Red = Red Reflectance

⚠️ Data Challenges
Noise: Due to cloud cover and imperfect labeling.

Missing Data: Caused by satellite obstruction (clouds).

Temporal Variation: NDVI values vary seasonally. You must apply feature engineering to capture meaningful trends.

🔍 Note:
Training and public test data contain noise. Private leaderboard data is clean. This setup evaluates your model’s generalization ability.

📂 Dataset
Each row in the dataset contains:

ID: Unique identifier for each sample.

class: Ground truth label — one of:
Water, Impervious, Farm, Forest, Grass, Orchard

27 NDVI Time Points:
Columns like 20150720_N, 20150602_N representing NDVI values collected over time.

📜 Rules
✅ Model: Only Logistic Regression (Multiclass) allowed.

✅ Allowed Preprocessing: Denoising, Imputation, Feature Engineering.

🧮 Leaderboard Structure:

Public Leaderboard (89%): Real-time feedback on submissions.

Private Leaderboard (11%): Used for final ranking to avoid overfitting.

🧮 Evaluation
Metric: Accuracy Score

Submission Format (CSV):

python-repl
Copy
Edit
ID,class
1,water
2,water
3,grass
4,impervious
...
🏅 Leaderboard Highlights
🥇 Model-2: Public Score 0.78546 (Best)

🥈 Model-5: Second Best

🥉 Model-3: Third Best

📁 Top Submissions:
SubmissionModel2.csv, SubmissionModel5.csv

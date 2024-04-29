# Cricket-K-means-Model
Artfully navigated the intricacies of data refinement, outlier treatment, and feature scaling. Employed a violin plot for outlier detection  and implemented meticulous data standardization. Forged a visually captivating k-means model, elucidating clusters with finesse.
The code involves data manipulation and analysis related to cricket statistics. 

1. **Data Loading and Information Extraction:**
   - The code snippet uses `df.info()` to load the dataset and extract information about the data types and memory usage.
   - The dataset includes columns such as 'Player,' 'Span,' 'Mat' (Matches), 'Inns' (Innings), 'NO' (Not Outs), 'Runs,' 'HS' (Highest Score), 'Ave' (Average), 'BF' (Balls Faced), 'SR' (Strike Rate), '100' (Centuries), '50' (Half-Centuries), '0' (Zero Scores), 'start,' and 'end.'
   - The code loads a dataset and extracts information about the data types and memory usage using df.info().

2. **Data Preprocessing:**
   - The code splits the 'Span' column into 'start' and 'end' columns to extract the start and end years of the players' careers.
   - It converts the 'start' and 'end' columns to integer type for further calculations.
   - The code calculates the experience of players by subtracting the start year from the end year and creates a new column 'Exp' to represent the years of experience.
   - It removes unnecessary columns like 'Span,' 'start,' and 'end' from the dataset to streamline the data for analysis.
   - The code splits a column named 'Span' into 'start' and 'end' columns using df[['start','end']]=df['Span'].str.split("-",expand=True).
   - It converts the 'start' and 'end' columns to integer type using df[['start','end']]=df[['start','end']].astype(int).
   - It calculates the experience of players by subtracting the 'start' year from the 'end' year and creates a new column 'Exp' using df['Exp']=df['end']-df['start'].
   - It removes the 'Span', 'start', and 'end' columns from the dataset using df.drop(['Span','start','end'],axis=1,inplace=True).
   - It removes the asterisk symbol from the 'HS' column using df['HS']=df['HS'].str.replace('*','').

3. **Data Analysis and Clustering:**
   - The dataset seems to contain detailed statistics of various cricket players, including their performance metrics like runs scored, average, strike rate, centuries, and half-centuries.
   - While the specific clustering algorithm applied is not explicitly mentioned in the provided snippet, the data appears to be structured for potential clustering analysis, possibly using K-means or other clustering techniques.
   - The code performs K-means clustering or other algorithms on the dataset for further analysis. However, the specific details of the clustering algorithm applied are not explicitly mentioned in the provided code snippet.

4. **Insights and Visualization:**
   - Further exploration of the dataset and potential visualization techniques could reveal patterns, trends, and insights into player performance, career spans, and other statistical aspects.
   - Visualizations like scatter plots, bar charts, or heatmaps could be utilized to present the data in a more understandable and insightful manner.
  
5. **Algorithms Applied:**
  - The code snippet does not explicitly mention the exact clustering algorithm applied (like K-means) or the clustering process details.
  - Further exploration of the code or additional context may provide more insights into the specific algorithm used.

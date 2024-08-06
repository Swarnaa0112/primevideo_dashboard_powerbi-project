
# Prime Video Insight Dashboard

### Dashboard Link: 

## Problem Statement

This dashboard helps Prime Video understand their subscribers' viewing habits and satisfaction levels. By analyzing different ratings and engagement metrics, Prime Video can identify areas for improvement and enhance the overall user experience. The dashboard also tracks content preferences, average watch times, and subscriber growth, enabling data-driven decisions to optimize content offerings and marketing strategies.

Since the number of neutral/dissatisfied subscribers (almost 57%) is more than satisfied subscribers (around 43%), Prime Video must focus on improving their services. Additionally, the average watch time and subscriber growth metrics highlight key areas for potential enhancement.

### Steps Followed

1. **Load Data**: Data was imported into Power BI Desktop from a CSV file containing subscriber and viewing information.
   
2. **Data Profiling**:
    - Opened Power Query Editor.
    - Enabled "Column Distribution," "Column Quality," and "Column Profile" options under the View tab.
    - Profiled columns based on the entire dataset.

3. **Data Cleaning**:
    - Identified and handled missing or erroneous values.
    - Specifically addressed null values in columns such as "Watch Time" and "Subscriber Ratings."

4. **Theme Selection**: Applied a suitable theme in the report view for visual consistency.

5. **Visualizations**:
    - Added visual filters (slicers) for "Genre," "Subscription Type," "Device Used," and "Region."
    - Created card visuals to represent key metrics such as average watch time and subscriber growth.
    - Used a bar chart to display the number of satisfied vs. neutral/unsatisfied subscribers, segmented by gender.
    - Represented different ratings (e.g., Content Quality, Streaming Quality, Customer Service) using a Ratings Visual.
    - Ignored zero values (not applicable) while calculating average ratings.

6. **Text and Graphics**:
    - Added text boxes for the Prime Video name and tagline.
    - Inserted a rectangle shape and the Prime Video logo for branding.

7. **Calculated Columns and Measures**:
    - Created a calculated column to group subscribers into various age groups using the following DAX expression:
    
      ```DAX
      Age Group = 
      IF(PrimeVideoData[Age] <= 25, "0-25",
      IF(PrimeVideoData[Age] <= 50, "25-50",
      IF(PrimeVideoData[Age] <= 75, "50-75", "75-100")))
      ```
    - Created measures for total subscriber count, percentage of subscribers by subscription type, and total watch time using DAX expressions.

8. **Publishing**: Published the report to Power BI Service.

## Insights

The dashboard provides the following insights:

### 1. Subscriber Demographics
- **Total Number of Subscribers**: 129,880
  - Satisfied Subscribers (Male): 21.68%
  - Satisfied Subscribers (Female): 21.76%
  - Neutral/Unsatisfied Subscribers (Male): 27.58%
  - Neutral/Unsatisfied Subscribers (Female): 28.97%
  - Higher number of subscribers are neutral/unsatisfied.

### 2. Average Ratings
- **Content Quality**: 4.1/5
- **Streaming Quality**: 3.9/5
- **Customer Service**: 3.7/5
- **Ease of Use**: 4.0/5
- **Recommendation Accuracy**: 3.8/5

### 3. Watch Time
- **Average Watch Time per Session**: 45 minutes
- **Peak Viewing Hours**: 7 PM - 10 PM

### 4. Subscriber Growth
- **Monthly New Subscribers**: 5,000
- **Churn Rate**: 3%

### 5. Content Preferences
- **Top Genres**:
  1. Action
  2. Drama
  3. Comedy
  4. Thriller
  5. Sci-Fi

### 6. Device Usage
- **Preferred Devices**:
  - Smart TV: 45%
  - Mobile: 30%
  - Tablet: 15%
  - Desktop: 10%

### 7. Regional Insights
- **Top Regions by Subscriber Count**:
  - North America: 40%
  - Europe: 30%
  - Asia: 20%
  - Other: 10%

### Additional Insights
- **Subscription Type**:
  - 50% of subscribers use monthly plans.
  - 50% use annual plans.
- **Age Group Distribution**:
  - 20% of subscribers are aged 0-25.
  - 50% are aged 25-50.
  - 25% are aged 50-75.
  - 5% are aged 75-100.


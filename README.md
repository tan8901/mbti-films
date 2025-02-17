# Film Characters & MBTI Personality Analysis
A data-driven analysis of the MBTIs of Characters in Popular Films.

## Introduction
Films are not just visual stories—they represent society through compelling characters, narratives, and emotions. A key driving force in films is the characters themselves. Their traits, mannerisms, and motivations can be analyzed using psychological tools, such as the **Myers-Briggs Type Indicator (MBTI)**, which classifies individuals into 16 personality types based on:

- **Introvert (I) vs. Extrovert (E)**
- **Sensing (S) vs. Intuitive (N)**
- **Thinking (T) vs. Feeling (F)**
- **Judging (J) vs. Perceiving (P)**

Classifying film characters by MBTI can reveal how their traits influence narrative development and audience resonance, impacting the film's popularity and success.

## Significance of the Study
Films influence public opinion, teach life lessons, and bring awareness to various issues. The main character and antagonist are crucial in shaping a film’s likability and viewer engagement. By exploring the relationship between character personality and film popularity, we can gain insights into the values and ideologies that resonate with society.

## Hypotheses & Expected Results
We propose the following hypotheses:

1. **Genre-based personality types**: Different genres may dominate with certain MBTI personality types.
2. **Timeline-based changes**: The dominant personality types for characters may evolve over time.
3. **Character relationships**: The relationship between the First Lead and Second Lead may influence their personality traits (opposite or identical).
4. **Consistent personality types**: Certain MBTI types may appear in films regardless of genre.

## Data Sources
- **IMDB Movies Dataset** (Accessed: 1st September 2024)  
  [IMDB Dataset](https://datasets.imdbws.com/)  
  The IMDB dataset provides movie information including title, average rating, number of ratings, and genre.
  
- **Personality Database (PDB)**  
  [Personality Database](https://www.personality-database.com/)  
  The PDB contains character information, including character name, movie title, MBTI personality type, and votes for each character.

1. **IMDB Dataset**: Used to collect movie details such as title, rating, and genre.
2. **PDB Scraping**: Scraped character profiles from PDB to obtain MBTI types and related votes for each movie character.

These datasets combined provide the necessary information for analyzing character personality and movie popularity.


## Scraping Methodology
We use **Selenium** and **Python** to automate web scraping and collect movie character data:

1. **Selenium**: Automates web browsing with Chrome WebDriver.
2. **Randomizing User Agents**: To prevent detection, we simulate user interaction by using multiple user agents.
3. **Meta Keywords**: Extracts character data by targeting the 'Movies' keyword in the HTML source.
4. **RegEx**: Matches specific data (e.g., character name, movie title, MBTI votes).
5. **Random Delays**: Introduces random delays between actions to mimic human browsing behavior.
6. **Batches**: Scrapes data in efficient batches, saving progress after each to reduce load on system resources.

Accessing the scraped dataset can be done through this link: <a name="https://drive.google.com/drive/folders/1SDU5CBjcQtdKyBlkpzRjrJS-S34zI1ZY?usp=sharing">Request Access</a>.

## Sample Visualizations

![image](https://github.com/user-attachments/assets/a4c10176-f328-4223-949a-d36a64aeb6e7)
![image](https://github.com/user-attachments/assets/cebcdd0e-f023-483e-a8be-6794deccb7c6)
![image](https://github.com/user-attachments/assets/196406ab-a0d4-4055-8771-da32247ed383)
![image](https://github.com/user-attachments/assets/ecd44bca-2ddb-4306-94a8-fa612b76a4be)
![image](https://github.com/user-attachments/assets/9927205f-0ca7-41e0-b9fd-50081157955e)
![image](https://github.com/user-attachments/assets/95f5069d-ba21-4352-adc4-c57c711a1295)

## Predictive Model
**Model 1:**

![image](https://github.com/user-attachments/assets/893d20a5-7aa6-4d18-a2bd-75cdf95dffde)

**Model 2:**

![image](https://github.com/user-attachments/assets/585dc618-b5ee-4e81-bda8-16003cfb664a)

**Predictors of Movie Popularity:**
- **Lead Character & Second Lead Character**: The popularity of the lead and second lead characters (measured by `lead_votes` and `secondlead_votes`) were the most significant predictors of movie popularity.
- **Genres**: Action, Adventure, Sci-Fi, Drama, and Thriller are the genres with the highest impact on film success.
- **MBTI Pairs**: 
  - **ISTJ-INFP**, **ISFJ-ENTP**, and **ISFP-ESTJ** were among the most predictive MBTI pairs.
  - Movies with introverted leads and extroverted second leads tend to perform better.
  - In the Romance genre, similar MBTI traits (matching personalities) appear to boost film popularity.
- **Relationships**: Enemy and Rival relationships between the lead characters contribute significantly to film popularity.

**Additional Insights:**
- **MBTI Pairs (Random Forest Model)**: INFP-INTJ emerged as a key MBTI pair, surpassing second lead votes in importance.
- **More Predictive MBTI Pairs**: 
  - ISFP-ESTJ, ENTP-ENTJ, ISTP-ENTP, and ISFP-ENFJ were also highly predictive.
- **Character Personality**: The most influential individual traits were **E** (Extroverted) and **I** (Introverted) for lead characters.
  
## Conclusion
- **Character Impact**: Characters and their personality types play a crucial role in determining the popularity of films.
- **Genre Influence**: Different genres favor specific personality types, with introverted characters dominant in darker genres like Drama and Action, while extroverted characters prevail in Comedy.
- **Time Trends**: Personality types for lead characters have shifted over time, especially in the 2000s and 2010s.
- **Character Dynamics**: The relationship between first and second leads often reflects complementary or opposing traits, influencing film success.
- **Consistent Traits**: Certain personality types (like ISFJ for second leads) remain consistent across genres, showing the influence of personality on film popularity.

By analyzing the personality types of characters across genres and time, we aim to uncover insights that shape film success, audience engagement, and societal impact.


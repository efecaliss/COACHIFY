# COACHIFY
Identifying Factors Affecting Student Retention in Coachify YKS Coaching Platform
1. Motivation & Background
Coachify is a YKS (university entrance exam) coaching platform designed to guide high school students and recent graduates through their exam preparation journey. The primary goal of this project is to investigate which factors most strongly influence student retention—how long students remain enrolled and actively engaged—so that we can refine mentor practices, enhance the overall service, and increase company revenue through better retention.
2. Project Objectives & Research Questions
Our main objective is to determine how various mentor- and student-related attributes correlate with a student’s decision to continue using the platform. By identifying which factors are most impactful, we can recommend strategic changes (e.g., optimizing session formats or frequencies) to improve retention.
Illustrative Research Questions:
Mentor’s YKS Ranking: Do mentors with a stronger national YKS performance tend to have students who remain longer in the program?
Meeting Format (Video vs. Voice): Are students more likely to continue if they have video-based sessions rather than voice-only?
Meeting Frequency & Session Length: Does higher frequency and/or longer session duration significantly boost retention?
Trial Session Success Rate: If a mentor’s trial sessions are successful (i.e., leads to a positive outcome for the student), does that mentor also see longer retention among enrolled students?
Mentor’s Subject Focus (Quantitative vs. Verbal): Does a mentor’s specialization align differently with student retention, e.g., do quantitative-focused mentors have higher or lower retention than verbally-focused mentors?
Student’s Academic Level (Grade): Are students in earlier grades (e.g., 11th) more or less likely to stay compared to those in 12th grade or graduates?
3. Data Description
We will primarily use our internal Coachify database, which contains (among other fields):
Student Name
Mentor Name
Grade Level
Membership Start Month
Membership Start Day
Dropped-Out Month
Additional data (e.g., session length, meeting format) will be collected via a short mentor survey. All personally identifiable information (names, contact details) will be anonymized or replaced with generic IDs to ensure privacy.
4. Key Factors to Be Analyzed
Based on preliminary discussion and domain knowledge, we will focus on these 7 factors:
Mentor’s YKS Ranking
Mentor’s Subject Focus (Quantitative vs. Verbal)
Meeting Frequency & Regularity
Session Length
Meeting Format (Video vs. Voice)
Mentor’s Trial Session Success Rate
Student’s Academic Level (Grade)
5. Analysis Plan
a) Data Collection & Preprocessing
Gathering and Merging
Import the database records (student enrollment info, dropout data) into a Pandas DataFrame (or similar format).
Collect mentor survey data (session length, format, frequency, YKS ranking) and merge it on the “Mentor Name” field.
Cleaning
Handle missing values (e.g., if some mentors did not provide session length).
Standardize formats (e.g., date fields into a single “start date” or “dropout date,” text for “Verbal” vs. “Quantitative,” etc.).
Anonymize personal identifiers (student and mentor names).
b) Exploratory Data Analysis (EDA)
Descriptive Statistics
Distribution of session lengths, frequency of meetings, average YKS ranking, etc.
Basic counts of students in each grade and how many months they stayed before dropping out.
Visualizations
Histograms or Boxplots for session length, meeting frequency.
Bar charts comparing average retention by subject focus or grade level.
Scatter plots to see if there’s an apparent relationship between mentor YKS ranking and retention.
Heatmap to visualize correlations among factors (if numeric enough) and with retention duration.
c) Hypothesis Testing & Statistical Analysis
Hypothesis Examples
H₀: “Meeting frequency has no significant impact on student retention.”
Hₐ: “Higher meeting frequency leads to significantly increased retention.”
Similar tests for session length, meeting format, etc.
Regression or Classification (Optional)
Regression (e.g., linear or logistic) to measure the influence of each factor on the number of months in the program or a binary outcome (stayed vs. dropped).
Evaluate model fit via R², RMSE, or classification metrics if using logistic regression.
Trend or Time-Series Analysis (If Relevant)
Explore whether certain months of membership correlate with dropouts (e.g., spike in dropout around a specific exam period).
d) Interpretation & Recommendations
Factor Ranking
Identify which variables show the strongest statistical relationship with retention.
Compare effect sizes or standardized coefficients to rank the factors.
Practical Recommendations
If, for instance, video calls show a significantly higher retention rate, propose guidelines for mentors to use video more frequently.
If the best YKS-ranked mentors consistently achieve higher retention, consider adjusting your mentor assignment or marketing approach.
6. Ethical & Privacy Considerations
All personally identifiable data will be removed.
Analyses and visualizations will only showcase aggregate trends.
The survey data from mentors will be kept confidential and used strictly for this analytical purpose.
7. Limitations & Future Work
Small Sample: Roughly 150 students and a limited set of mentors (about 40) may restrict the breadth of statistical power.
Survey Accuracy: Mentors’ self-reported session lengths or frequency might contain biases.
Excluded Factors: We do not measure personal motivation directly, which can also heavily influence retention.
Potential Next Steps:
Implement changes (e.g., recommended session frequency or format) based on findings.
Monitor the impact on retention over subsequent months to validate results.
8. Conclusion
By systematically analyzing these seven key factors, we aim to pinpoint which mentor and student attributes most strongly influence continued enrollment in Coachify’s YKS coaching services. These insights will be critical in refining mentor practices, guiding future platform features, and ultimately enhancing both student success and the company’s profitability.

# Engineering Exam Selection Analysis

#### (Analysis in Jupyter Notebook)
### The Problem

The prediction of wether a student is likely to be selected in an College of desire based on various factors like Mother tongue, Hours of Study etc. Data of students who persued engineering and how many of them got in needs to be converted into appropriate form to be used in an Linear Regression Model. The non-numeric data has to be converved into numeric

### The Input Data

The data for the training of the model was collected using a Google Form. All the relevant fields were made compulsory. The Form was provided to student who persued Engineering and weather they are in IIT or not was also asked.
A total of 150(100 – training,50 - testing) samples were obtained (a very small dataset). 

### The Manipulation of Data and the Model

Every data field (Features)  is analysed and visualized using matplotlib ,seaborn and pandas. A normal graph is used to plot numeric fields and a pie for the binary ones.

#### 1. Parent Income Per Annum
The Income of each of the Sample is collected in LPA.
A higher income indicates that not only does the student has access to better education but is likely to be able to take advantage of further resources like Couching Classes, Books, Sample ware etc.

#### 2. Mother Tongue
Although this my not be apparent but the languages or medium of the enterance  exam are Hindi and English. The students who have eng or hindi are more likely to be able to understand the paper.
The data is not numeric. The data is converted into binary form with hindi/eng and others being replaced by 1 and 0 respectively.[using df.e(‘hindi’ or ‘english’).mal(1)]

#### 3. Percent In Class 12
The students have to obtain a minimum of 75%. The percentage is also factored in while calculating wether you qualify for the advance. 40% of the ranking  is calculated from your 12th grade marks. Also, A student witha a higher percentage is also more likely to score more everyware else. 

#### 4. Avg Number of Hrs Studied
A student who spends more time in study and practice is more likely to develop the relevant skills. 

#### 5. State
The state in which the student lives may have better  school or the correct environment  to nurture bright minds.

#### 6. School Location Area
The location of where the student lives or studies has a influence on the resouces they get.A student in an urban area is likely to have access to better education and help. 
The data is Binary. The data is converted into numeric form with Male and Female being replaced by 1 and 0 respectively.[using df.e(‘Urban’).mal(1)]
 
### Model
1. The numeric data is analysed using df.describe(). The Binary data is represented in pie charts and the rest are plotted in normal graphs.
2. The mean and minimum values are represented with horizontal liines.
3. The non-numeric and binary data were converted into 1s and 0s.
4. The ‘mother tongue’  is distributed into dummie fields.
5. Use pairplot and corr are used to see if the features are linear dependence or not. Elininate one if they are.
6. All the features are made into a single dateframe and the predictant
7. Missing values are checked for 
 
### Result
The linear regressi had a score of **73.54 %** obtained from 100 samples(which is a very small dataset).

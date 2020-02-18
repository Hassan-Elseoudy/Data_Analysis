# Data Analysis.

## What is Data Analysis?
#### 1. Questions
Either you're given data and ask questions based on it, or you ask questions first and gather data based on that later. In both cases, great questions help you focus on relevant parts of your data and direct your analysis towards meaningful insights.

#### 2. Wrangle
You get the data you need in a form you can work with in three steps: **gather, assess and clean**. You gather the data you need to answer your questions, assess your data to identify any problems in your data’s quality or structure, and clean your data by **modifying, replacing, or removing data** to ensure that your dataset is of the highest quality and as well-structured as possible.

#### 3. Perform EDA (Exploratory Data Analysis)
You explore and then augment your data to maximize the potential of your analyses, visualizations, and models. Exploring involves **finding patterns in your data, visualizing relationships in your data, and building intuition about what you’re working with.** After exploring, you can do things like **remove outliers and create better features from your data**, also known as feature engineering.

#### 4. Draw Conclusions
This step is typically approached with machine learning or inferential statistics.

#### 5. Communicate
You often need to justify and convey meaning in the insights you’ve found. Or, if your end goal is to build a system, you usually need to share what you’ve built, explain how you reached design decisions, and report how well it performs. There are many ways to communicate your results: reports, slide decks, blog posts, emails, presentations, or even conversations. Data visualization will always be very valuable.


<div ><h2 id="Descriptive Statistics I">Descriptive Statistics I</h2>
<p>The table below summarizes our data types.  To expand on the information in the table, you can look through the text that follows.</p>
<div class="index-module--table-responsive--1zG6k"><table class="index-module--table--8j68C index-module--table-striped--3HHC-">
<thead>
<tr>
<th><strong>Data Types</strong></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Quantitative:</strong></td>
<td><strong>Continuous</strong></td>
<td><strong>Discrete</strong></td>
</tr>
<tr>
<td></td>
<td>Height, Age, Income</td>
<td>Pages in a Book,  Trees in Yard, Dogs at a Coffee Shop</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td><strong>Categorical:</strong></td>
<td><strong>Ordinal</strong></td>
<td><strong>Nominal</strong></td>
</tr>
<tr>
<td></td>
<td>Letter Grade,  Survey Rating</td>
<td>Gender, Marital Status, Breakfast Items</td>
</tr>
</tbody>
</table>
</div><p>Below is a little more detail of the information shared in the above table.</p>
<h2 id="another-look">Another Look</h2>
<p>To break down our data types, there are two main blocks:</p>
<p><strong>Quantitative</strong> and <strong>Categorical</strong></p>
<p><strong>Quantitative</strong> can be further divided into <code>Continuous</code> or <code>Discrete</code>.</p>
<p><strong>Categorical</strong> data can be divided into <code>Ordinal</code> or <code>Nominal</code>.  </p>
<p>You should have now mastered what types of data in the world around us falls into each of these four buckets: Discrete, Continuous, Nominal, and Ordinal.  In the next sections, we will work through the numeric summaries that relate specifically to quantitative variables. </p>
<hr>
<h2 id="quantitative-vs-categorical">Quantitative vs. Categorical</h2>
<p>Some of these can be a bit tricky - notice even though zip codes are a number, they aren’t really a quantitative variable.  If we add two zip codes together, we do not obtain any useful information from this new value.  Therefore, this is a categorical variable.   </p>
<p><strong>Height</strong>, <strong>Age</strong>, the <strong>Number of Pages in a Book</strong> and <strong>Annual Income</strong> all take on values that we can add, subtract and perform other operations with to gain useful insight.  Hence, these are <code>quantitative</code>.  </p>
<p><strong>Gender</strong>, <strong>Letter Grade</strong>, <strong>Breakfast Type</strong>, <strong>Marital Status</strong>, and <strong>Zip Code</strong> can be thought of as labels for a group of items or individuals. Hence, these are <code>categorical</code>.</p>
<hr>
<h2 id="continuous-vs-discrete">Continuous vs. Discrete</h2>
<p>To consider if we have continuous or discrete data, we should see if we can split our data into smaller and smaller units.  Consider time - we could measure an event in years, months, days, hours, minutes, or seconds, and even at seconds we know there are smaller units we could measure time in.  Therefore, we know this data type is continuous.  <strong>Height</strong>, <strong>age</strong>, and <strong>income</strong> are all examples of <code>continuous data</code>. Alternatively, the <strong>number of pages in a book</strong>, <strong>dogs I count outside a coffee shop</strong>, or <strong>trees in a yard</strong> are <code>discrete data</code>.  We would not want to split our dogs in half.</p>
<hr>
<h2 id="ordinal-vs-nominal">Ordinal vs. Nominal</h2>
<p>In looking at categorical variables, we found <strong>Gender</strong>, <strong>Marital Status</strong>, <strong>Zip Code</strong> and your <strong>Breakfast items</strong> are <code>nominal variables</code> where there is no order ranking associated with this type of data.  Whether you ate cereal, toast, eggs, or only coffee for breakfast; there is no rank ordering associated with your breakfast.  </p>
<p>Alternatively, the <strong>Letter Grade</strong> or <strong>Survey Ratings</strong> have a rank ordering associated with it, as <code>ordinal data</code>.  If you receive an A, this is higher than an A-.  An A- is ranked higher than a B+, and so on...  Ordinal variables frequently occur on rating scales from very poor to very good.  In many cases we turn these ordinal variables into numbers, as we can more easily analyze them.</p>
<hr>
<h2 id="final-words">Final Words</h2>
<p>In this section, we looked at the different data types we might work with in the world around us.  When we work with data in the real world, it might not be very clean - sometimes there are typos or missing values.  When this is the case, simply having some expertise regarding the data and knowing the data type can assist in our ability to ‘clean’ this data.  Understanding data types can also assist in our ability to build visuals to best explain the data.</p>
</div></div>

<div >
<h2 id="analyzing-quantitative-data">Analyzing Quantitative Data</h2>
<h4 id="four-aspects-for-quantitative-data">Four Aspects for Quantitative Data</h4>
<p>There are four main aspects to analyzing <strong>Quantitative</strong> data.  </p>
<ol>
<li>Measures of <code>Center</code></li>
<li>Measures of <code>Spread</code></li>
<li>The <code>Shape</code> of the data.</li>
<li><code>Outliers</code></li>
</ol>
<h4 id="analyzing-categorical-data">Analyzing Categorical Data</h4>
<p>Analyzing categorical data has fewer parts to consider.  <strong>Categorical</strong> data is analyzed usually by looking at the counts or proportion of individuals that fall into each group.  For example if we were looking at the breeds of the dogs, we would care about how many dogs are of each breed, or what proportion of dogs are of each breed type.</p>
<h2 id="measures-of-center">Measures of Center</h2>
<p>There are three measures of center:</p>
<ol>
<li><code>Mean</code></li>
<li><code>Median</code></li>
<li><code>Mode</code></li>
</ol>
<h2 id="the-mean">The Mean</h2>
<p>The mean is often called the average or the <strong>expected value</strong> in mathematics.  We calculate the mean by adding all of our values together, and dividing by the number of values in our dataset.</p>
</div>

<div <h2 id="the-median">The Median</h2>
<p>The <strong>median</strong> splits our data so that 50% of our values are lower and 50% are higher.  We found how we calculate the median depends on if we have an even number of observations or an odd number of observations. </p>
<h4 id="median-for-odd-values">Median for Odd Values</h4>
<p>If we have an <strong>odd</strong> number of observations, the <strong>median</strong> is simply the number in the <strong>direct middle</strong>.  For example, if we have 7 observations, the median is the fourth value when our numbers are ordered from smallest to largest.  If we have 9 observations, the median is the fifth value.  </p>
<h4 id="median-for-even-values">Median for Even Values</h4>
<p>If we have an <strong>even</strong> number of observations, the <strong>median</strong> is the <strong>average of the two values in the middle</strong>.  For example, if we have 8 observations, we average the fourth and fifth values together when our numbers are ordered from smallest to largest.  </p>
  <p>In order to compute the median we <b>MUST</b> sort our values first.  </p>
<p>Whether we use the mean or median to describe a dataset is largely dependent on the <strong>shape</strong> of our dataset and if there are any <strong>outliers</strong>.</p>
</div></div></div></div>

<div <h2 id="the-mode">The Mode</h2>
<p>The <strong>mode</strong> is the most frequently observed value in our dataset.  </p>
<p>There might be multiple modes for a particular dataset, or no mode at all.  </p>
<h4 id="no-mode">No Mode</h4>
<p>If all observations in our dataset are observed with the same frequency, there is no mode.  If we have the dataset: </p>
<p>1, 1, 2, 2, 3, 3, 4, 4</p>
<p>There is no mode, because all observations occur the same number of times.  </p>
<h4 id="many-modes">Many Modes</h4>
<p>If two (or more) numbers share the maximum value, then there is more than one mode.  If we have the dataset:</p>
<p>1, 2, 3, 3, 3, 4, 5, 6, 6, 6, 7, 8, 9 </p>
<p>There are two modes 3 and 6, because these values share the maximum frequencies at 3 times, while all other values only appear once.  </p>
</div></div></div></div>

<div ></div><div <h2 id="notation">Notation</h2>
<p>Notation is a common language used to communicate mathematical ideas.  <strong>Think of notation as a universal language used by academic and industry professionals to convey mathematical ideas.</strong></p>
<p>You likely already know some notation.  Plus, minus, multiply, division, and equal signs all have mathematical symbols that you are likely familiar with.  Each of these symbols replaces an idea for how numbers interact with one another. it does have the following properties:</p>
<ol>
<li><p><strong>Understanding how to correctly use notation makes you seem really smart.</strong>  Knowing how to read and write in notation is like learning a new language.  A language that is used to convey ideas associated with mathematics.  <br><br></p>
</li>
<li><p><strong>It allows you to read documentation, and implement an idea to your own problem.</strong>   Notation is used to convey how problems are solved all the time.  One really popular mathematical algorithm that is used to solve some of the world's most difficult problems is known as Gradient Boosting.  The way that it solves problems is explained here: <a target="_blank" href="https://en.wikipedia.org/wiki/Gradient_boosting">https://en.wikipedia.org/wiki/Gradient_boosting</a>.  If you really want to understand how this algorithm works, you need to be able to read and understand notation.  <br><br></p>
</li>
<li><p><strong>It makes ideas that are hard to say in words easier to convey.</strong>   Sometimes we just don't have the right words to say.  For those situations, I prefer to use notation to convey the message.  Similar to the way an emoji or meme might convey a feeling better than words, notation can convey an idea better than words.  Usually those ideas are related to mathematics, but I am not here to stifle your creativity.</p>
</li>
</ol>
</div></div></div></div></div>

<div ><div <h2 id="example-to-introduce-notation">Example to Introduce Notation</h2>
<h4 id="rows-and-columns">Rows and Columns</h4>
<p>Spreadsheets are a common way to hold data.  They are composed of rows and columns.  Rows run horizontally, while columns run vertically.  Each column in a spreadsheet commonly holds a specific <strong>variable</strong>, while each row is commonly called an <strong>instance</strong> or <strong>individual</strong>.  </p>
<div class="index-module--table-responsive--1zG6k"><table class="index-module--table--8j68C index-module--table-striped--3HHC-">
<thead>
<tr>
<th><strong>Date</strong></th>
<th><strong>Day of Week</strong></th>
<th><strong>Time Spent On Site</strong> (<strong>X</strong>)</th>
<th><strong>Buy</strong> (<strong>Y</strong>)</th>
</tr>
</thead>
<tbody>
<tr>
<td>June 15</td>
<td>Thursday</td>
<td>5</td>
<td>No</td>
</tr>
<tr>
<td>June 15</td>
<td>Thursday</td>
<td>10</td>
<td>Yes</td>
</tr>
<tr>
<td>June 16</td>
<td>Friday</td>
<td>20</td>
<td>Yes</td>
</tr>
</tbody>
</table>
</div><p>This is a <strong>row</strong>:</p>
<div class="index-module--table-responsive--1zG6k"><table class="index-module--table--8j68C index-module--table-striped--3HHC-">
<thead>
<tr>
<th><strong>Date</strong></th>
<th><strong>Day of Week</strong></th>
<th><strong>Time Spent On Site</strong> (<strong>X</strong>)</th>
<th><strong>Buy</strong> (<strong>Y</strong>)</th>
</tr>
</thead>
<tbody>
<tr>
<td>June 15</td>
<td>Thursday</td>
<td>5</td>
<td>No</td>
</tr>
</tbody>
</table>
</div><p>This is a <strong>column</strong>:</p>
<div class="index-module--table-responsive--1zG6k"><table class="index-module--table--8j68C index-module--table-striped--3HHC-">
<thead>
<tr>
<th><strong>Time Spent On Site</strong> (<strong>X</strong>)</th>
</tr>
</thead>
<tbody>
<tr>
<td>5</td>
</tr>
<tr>
<td>10</td>
</tr>
<tr>
<td>20</td>
</tr>
</tbody>
</table>
</div><h4 id="before-collecting-data">Before Collecting Data</h4>
<p><strong>Before collecting data, we usually start with a question, or many questions, that we would like to answer.  The purpose of data is to help us in answering these questions.</strong></p>
<h4 id="random-variables">Random Variables</h4>
<p>A <strong>random variable</strong> is a placeholder for the possible values of some process (mostly... the term 'some process' is a bit ambiguous).  As was stated before, notation is useful in that it helps us take complex ideas and simplify (often to a single letter or single symbol).  We see random variables represented by capital letters (<strong>X</strong>, <strong>Y</strong>, or <strong>Z</strong> are common ways to represent a random variable). </p>
<p>We might have the random variable <strong>X</strong>, which is a holder for the possible values of the amount of time someone spends on our site.  Or the random variable <strong>Y</strong>, which is a holder for the possible values of whether or not an individual purchases a product.  </p>
<p><strong>X</strong> is 'a holder' of the values that could possibly occur for the amount of time spent on our website.  Any number from 0 to infinity really.  </p>
</div></div></div></div></div>

<div ><div <h2 id="capital-vs-lower-case-letters">Capital vs. Lower Case Letters</h2>
<p><strong>Random variables</strong> are represented by capital letters.  Once we observe an outcome of these random variables, we notate it as a lower case of the same letter.  </p>
<h4 id="example-1">Example 1</h4>
<p>For example, the <strong>amount of time someone spends on our site</strong> is a <strong>random variable</strong> (we are not sure what the outcome will be for any particular visitor), and we would notate this with <strong>X</strong>.  Then when the first person visits the website, if they spend 5 minutes, we have now observed this outcome of our random variable.  We would notate any outcome as a lowercase letter with a subscript associated with the order that we observed the outcome.    </p>
<p>If 5 individuals visit our website, the first spends 10 minutes, the second spends 20 minutes, the third spends 45 mins, the fourth spends 12 minutes, and the fifth spends 8 minutes; we can notate this problem in the following way:</p>
<p><strong>X</strong> is the amount of time an individual spends on the website.</p> 
  <p><b>x<sub>1</sub></b> = 10,  <b>x<sub>2</sub></b> = 20,  <b>x<sub>3</sub></b> = 45,  <b>x<sub>4</sub></b> = 12,
    <b>x<sub>5</sub></b> = 8.</p> <p>The capital <strong>X</strong> is associated with this idea of a <strong>random variable</strong>, while the observations of the random variable take on lowercase <strong>x</strong> values.  </p>
<h4 id="example-2">Example 2</h4>
<p>Taking this one step further, we could ask: </p>
<p><strong>What is the probability someone spends more than 20 minutes in our website?</strong></p>
<p>In notation, we would write:</p>
<p><strong>P(X &gt; 20)?</strong></p>
<p>Here <strong>P</strong> stands for <strong>probability</strong>, while the parentheses encompass the statement for which we would like to find the probability.  Since <strong>X</strong> represents the amount of time spent on the website, this notation represents the probability the amount of time on the website is greater than 20.  </p>
<p>We could find this in the above example by noticing that only one of the 5 observations exceeds 20.  So, we would say there is a <strong>1</strong> (the 45) <strong>in 5 or 20%</strong> chance that an individual spends more than 20 minutes on our website (based on this dataset).  </p>
<h4 id="example-3">Example 3</h4>
<p>If we asked: <strong>What is the probability of an individual spending 20 or more minutes on our website?</strong> We could notate this as:</p>
<p><strong>P(X ≥ 20)?</strong></p>
<p>We could then find this by noticing there are two out of the five individuals that spent 20 or more minutes on the website.  So this probability is <strong>2 out of 5 or 40%</strong>.</p>
</div></div></div></div></div>

<div <h2 id="notation-for-calculating-the-mean">Notation for Calculating the Mean</h2>
<p>We know that the mean is calculated as the sum of all our values divided by the number of values in our dataset.  </p>
<p>In our current notation, adding all of our values together can be extremely tedious.  If we want to add 3 values of some random variable together, we would use the notation:</p>
  <p><b>x<sub>1</sub></b> + <b>x<sub>2</sub></b> + <b>x<sub>3</sub></b></p>
<p>If we want to add 6 values together, we would use the notation:</p>
  <p><b>x<sub>1</sub></b> + <b>x<sub>2</sub></b> + <b>x<sub>3</sub></b> + <b>x<sub>4</sub></b> + <b>x<sub>5</sub></b> + <b>x<sub>6</sub></b></p>
<p>To extend this to add one hundred, one thousand, or one million values would be ridiculous!  How can we make this easier to communicate?!</p>
</div></div></div></div>
<div >

## Aggregations

An **aggregation** is a way to turn multiple numbers into fewer numbers (commonly one number).

**Summation** is a common aggregation. The notation used to sum our values is a greek symbol called sigma **Σ**.

#### Example 1

Imagine we are looking at the amount of time individuals spend on our website. We collect data from nine individuals:
If we want to sum the **first three values** together In our new notation, we can write:

<img src = 'https://latex.codecogs.com/gif.latex?%5Csum_%7Bi%3D1%7D%5E%7Bi%3D3%7Dx_%7Bi%7D'>

#### Other Aggregations

The **Σ** sign is used for aggregating using summation, but we might choose to aggregate in other ways. Summing is one of the most common ways to need to aggregate. However, we might need to aggregate in alternative ways. If we wanted to multiply all of our values together we would use a product sign **Π** , capital Greek letter pi. The way we aggregate continuous values is with something known as integration (a common technique in calculus), which uses the following symbol **∫**
</div>

<div <h2 id="final-steps-for-calculating-the-mean">Final Steps for Calculating the Mean</h2>
<p>To finalize our calculation of the mean, we introduce <strong>n</strong> as the total number of values in our dataset.  We can use this notation both at the top of our summation, as well as for the value that we divide by when calculating the mean.  </p>
  
<img src = 'https://latex.codecogs.com/gif.latex?%5Cfrac%7B1%7D%7Bn%7D%5Csum_%7Bi%3D1%7D%5E%7Bi%3Dn%7Dx_%7Bi%7D'>
<p>Instead of writing out all of the above, we commonly write <b>x̄</b> to represent the mean of a dataset.
<hr>
<h2 id="Basic SQL">Basic SQL</h2>
<h3 id="entity-relationship-diagrams">Entity Relationship Diagrams</h3>
<p>An <strong>entity relationship diagram</strong> (ERD) is a common way to view data in a database.  Below is the ERD for the database we will use from Parch &amp; Posey.  These diagrams help you visualize the data you are analyzing  including:</p>
<ol>
<li>The names of the tables.</li>
<li>The columns in each table.</li>
<li>The way the tables work together.  </li>
</ol>
<p><strong>You can think of each of the boxes below as a spreadsheet.</strong></p>
</div></div><span></span></div></div></div><div><div ><h3 id="what-to-notice">What to Notice</h3>
<p>In the Parch &amp; Posey database there are five tables (essentially 5 spreadsheets): </p>
<ol>
<li><strong>web_events</strong></li>
<li><strong>accounts</strong></li>
<li><strong>orders</strong></li>
<li><strong>sales_reps</strong></li>
<li><strong>region</strong> </li>
</ol>
<p>You can think of each of these tables as an individual spreadsheet.  Then the columns in each spreadsheet are listed below the table name.  For example, the <strong>region</strong> table has two columns: <code>id</code> and <code>name</code>.  Alternatively the <strong>web_events</strong> table has four columns.</p>
</div></div><span></span></div></div></div><div><div crow's foot" that connects the tables together shows us how the columns in one table relate to the columns in another table.  In this first lesson, you will be learning the basics of how to work with SQL to interact with a single table.</p>
</div></div><span></span></div></div></div></div>
<hr>
<div ><h2 id="introduction">Introduction</h2>
<p>Before we dive into writing Structured Query Language (SQL) queries, let's take a look at what makes SQL and the databases that utilize SQL so popular.  </p>
<p>I think it is an important distinction to say that SQL is a <strong>language</strong>.  Hence, the last word of SQ<strong>L</strong> being <strong>language</strong>.  SQL is used all over the place beyond the databases we will utilize in this class.  With that being said, SQL is most popular for its interaction with databases.  For this class, you can think of a <strong>database</strong> as a bunch of excel spreadsheets all sitting in one place.  Not all databases are a bunch of excel spreadsheets sitting in one place, but it is a reasonable idea for this class.</p>
  <hr>
<h2 id="why-do-data-analysts-use-sql-">Why Do Data Analysts Use SQL?</h2>
<p>There are some major advantages to using <strong>traditional relational databases,</strong> which we interact with using SQL. The five most apparent are:</p>
<ul>
<li>SQL is easy to understand.</li>
<li>Traditional databases allow us to access data directly.</li>
<li>Traditional databases allow us to audit and replicate our data.</li>
<li>SQL is a great tool for analyzing multiple tables at once.</li>
<li>SQL allows you to analyze more complex questions than dashboard tools like Google Analytics.</li>
</ul>
</div>
  <hr>
<h2 id="why-do-businesses-choose-sql-">Why Do Businesses Choose SQL?</h2>
<ol>
<li><p><strong>Data integrity is ensured</strong> - only the data you want entered is entered, and only certain users are able to enter data into the database. <br><br></p>
</li>
<li><p><strong>Data can be accessed quickly</strong> - SQL allows you to obtain results very quickly from the data stored in a database.  Code can be optimized to quickly pull results.  <br><br></p>
</li>
<li><p><strong>Data is easily shared</strong> - multiple individuals can access data stored in a database, and the data is the same for all users allowing for consistent results for anyone with access to your database.</p>
</li>
</ol>
</div></div><span></span></div></div></div></div>
<hr>
<div <p>A few key points about data stored in SQL databases:</p>
<ol>
<li><p><strong>Data in databases is stored in tables that can be thought of just like Excel spreadsheets.</strong> <br>For the most part, you can think of a database as a bunch of Excel spreadsheets.  Each spreadsheet has rows and columns.  Where each row holds data on a transaction, a person, a company, etc., while each column holds data pertaining to a particular aspect of one of the rows you care about like a name, location, a unique id, etc.<br><br></p>
</li>
<li><p><strong>All the data in the same column must match in terms of data type. </strong> <br>An entire column is considered quantitative, discrete, or as some sort of string.  This means if you have one row with a string in a particular column, the entire column might change to a text data type.  <strong>This can be very bad if you want to do math with this column!</strong><br><br></p>
</li>
<li><p><strong>Consistent column types are one of the main reasons working with databases is fast.</strong> <br>Often databases hold <strong>a LOT</strong> of data.  So, knowing that the columns are all of the same type of data means that obtaining data from a database can still be fast.<br><br></p>
</li>
</ol>
</div></div></div></div>
<hr>

## Statements
<div class="index-module--table-responsive--1zG6k"><table class="index-module--table--8j68C index-module--table-striped--3HHC-">
<thead>
<tr>
<th><strong>Statement</strong></th>
<th><strong>How to Use It</strong></th>
<th><strong>Other Details</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>SELECT</td>
<td>SELECT <strong>Col1</strong>, <strong>Col2</strong>, ...</td>
<td>Provide the columns you want</td>
</tr>
<tr>
<td>FROM</td>
<td>FROM <strong>Table</strong></td>
<td>Provide the table where the columns exist</td>
</tr>
<tr>
<td>LIMIT</td>
<td>LIMIT <strong>10 </strong></td>
<td>Limits based number of rows returned</td>
</tr>
<tr>
<td>ORDER BY</td>
<td>ORDER BY <strong>Col</strong></td>
<td>Orders table based on the column.  Used with <strong>DESC</strong>.</td>
</tr>
<tr>
<td>WHERE</td>
<td>WHERE <strong>Col &gt; 5</strong></td>
<td>A conditional statement to filter your results </td>
</tr>
<tr>
<td>LIKE</td>
<td>WHERE <strong>Col LIKE '%me%'</strong></td>
<td>Only pulls rows where column has 'me' within the text </td>
</tr>
<tr>
<td>IN</td>
<td>WHERE <strong>Col IN ('Y', 'N')</strong></td>
<td>A filter for only rows with column of 'Y' or 'N'</td>
</tr>
<tr>
<td>NOT</td>
<td>WHERE <strong>Col NOT IN ('Y', 'N')</strong></td>
<td><strong>NOT</strong> is frequently used with <strong>LIKE</strong> and <strong>IN</strong></td>
</tr>
<tr>
<td>AND</td>
<td>WHERE <strong>Col1 &gt; 5 AND Col2 &lt; 3 </strong></td>
<td>Filter rows where two or more conditions must be true </td>
</tr>
<tr>
<td>OR</td>
<td>WHERE <strong>Col1 &gt; 5 OR Col2 &lt; 3</strong></td>
<td>Filter rows where at least one condition must be true</td>
</tr>
<tr>
<td>BETWEEN</td>
<td>WHERE <strong>Col BETWEEN 3 AND 5</strong></td>
<td>Often easier syntax than using an <strong>AND</strong></td>
</tr>
</tbody>
</table>
</div><h3 id="other-tips">Other Tips</h3>
<p>Though SQL is <strong>not case sensitive</strong> (it doesn't care if you write your statements as all uppercase or lowercase), we discussed some best practices.  <strong>The order of the key words does matter!</strong>  Using what you know so far, you will want to write your statements as:</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> col1, col2
<span class="hljs-keyword">FROM</span> table1
<span class="hljs-keyword">WHERE</span> col3  &gt; <span class="hljs-number">5</span> <span class="hljs-keyword">AND</span> col4 <span class="hljs-keyword">LIKE</span> <span class="hljs-string">'%os%'</span>
<span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> col5
<span class="hljs-keyword">LIMIT</span> <span class="hljs-number">10</span>;</span>
</code></pre><p>Notice, you can retrieve different columns than those being used in the <strong>ORDER BY</strong> and <strong>WHERE</strong> statements.  Assuming all of these column names existed in this way (<code>col1</code>, <code>col2</code>, <code>col3</code>, <code>col4</code>, <code>col5</code>) within a table called <code>table1</code>, this query would run just fine.</p>
</div>

<hr>

<div>
<h3 id="primary-and-foreign-keys">Primary and Foreign Keys</h3>
<p>You learned a key element for <strong>JOIN</strong>ing tables in a database has to do with primary and foreign keys:</p>
<ul>
<li><p><strong>primary keys</strong> - are unique for every row in a table.  These are generally the first column in our database (like you saw with the <strong>id</strong> column for every table in the Parch &amp; Posey database).</p>
</li>
<li><p><strong>foreign keys</strong> - are the <strong>primary key</strong> appearing in another table, which allows the rows to be non-unique.  </p>
</li>
</ul>
<p>Choosing the set up of data in our database is very important, but not usually the job of a data analyst.  This process is known as <strong>Database Normalization</strong>.</p>
<h3 id="joins">JOINs</h3>
<p>In this lesson, you learned how to combine data from multiple tables using <strong>JOIN</strong>s.  The three <strong>JOIN</strong> statements you are most likely to use are:</p>
<ol>
<li><strong>JOIN</strong> - an <strong>INNER JOIN</strong> that only pulls data that exists in both tables.</li>
<li><strong>LEFT JOIN</strong> - pulls all the data that exists in both tables, as well as all of the rows from the table in the <strong>FROM</strong> even if they do not exist in the <strong>JOIN</strong> statement.</li>
<li><strong>RIGHT JOIN</strong> - pulls all the data that exists in both tables, as well as all of the rows from the table in the <strong>JOIN</strong> even if they do not exist in the <strong>FROM</strong> statement.</li>
</ol>
<p>There are a few more advanced <strong>JOIN</strong>s that we did not cover here, and they are used in very specific use cases.  <a target="_blank" href="https://www.w3schools.com/sql/sql_union.asp">UNION and UNION ALL</a>, <a target="_blank" href="http://www.w3resource.com/sql/joins/cross-join.php">CROSS JOIN</a>, and the tricky <a target="_blank" href="https://www.w3schools.com/sql/sql_join_self.asp">SELF JOIN</a>.  These are more advanced than this course will cover, but it is useful to be aware that they exist, as they are useful in special cases.</p>
<h3 id="alias">Alias</h3>
<p>This allows to be more efficient in the number of characters needed to write.</p>
<hr>
  
  <div ><h2 id="Descriptive Statistics II">Descriptive Statistics II</h2>

  
  <div <h2 id="measures-of-spread">Measures of Spread</h2>
<p><strong>Measures of Spread</strong> are used to provide us an idea of how spread out our data are from one another.  Common measures of spread include:</p>
<ol>
<li><strong>Range</strong></li>
<li><strong>Interquartile Range (IQR)</strong></li>
<li><strong>Standard Deviation</strong></li>
<li><strong>Variance</strong></li>
</ol>
</div></div></div></div>
<hr>

<div ><div <h2 id="histograms">Histograms</h2>
<p>Histograms are super useful to understanding the different aspects of quantitative data.  In the upcoming concepts, you will see histograms used all the time to help you understand the four aspects we outlined earlier regarding a quantitative variable: </p>
<ul>
<li>center</li>
<li>spread</li>
<li>shape</li>
<li>outliers</li>
</ul>
</div></div></div></div></div>

<hr>

<div <h2 id="calculating-the-5-number-summary">Calculating the 5 Number Summary</h2>
<p>The five number summary consist of 5 values:</p>
<ol>
<li><strong>Minimum:</strong> The smallest number in the dataset.</li>
<li><b>Q<sub>1</sub></b>: The value such that 25% of the data fall below.</li>
<li><b>Q<sub>2</sub></b>: The value such that 50% of the data fall below.</li>
<li><b>Q<sub>3</sub></b>: The value such that 75% of the data fall below.</li>
<li><strong>Maximum:</strong> The largest value in the dataset.</li>
</ol>
<p>In the above video we saw that calculating each of these values was essentially just finding the median of a bunch of different dataset.  Because we are essentially calculating a bunch of medians, the calculation depends on whether we have an odd or even number of values.  </p>
<h2 id="range">Range</h2>
<p>The <strong>range</strong> is then calculated as the difference between the <strong>maximum</strong> and the <strong>minimum</strong>.  </p>
<h2 id="iqr">IQR</h2>
<p>The <strong>interquartile range</strong> is calculated as the difference between <b>Q<sub>3</sub></b> and <b>Q<sub>1</sub></b>
</div></div></div></div>

<hr>

<div ><h3>Standard Deviation and Variance</h3>
<p>The <strong>standard deviation</strong> is one of the most common measures for talking about the spread of data.  It is defined as <strong>the average distance of each observation from the mean</strong>.  </p>
</div>

<hr>

<h2 id="shape">Shape</h2>
<p>We learned that the distribution of our data is frequently associated with one of the three <strong>shapes</strong>:</p>
<p><strong>1. Right-skewed</strong></p>
<p><strong>2. Left-skewed</strong></p>
<p><strong>3. Symmetric</strong> (frequently normally distributed)</p>
<p>Depending on the shape associated with our dataset, certain measures of center or spread may be better for summarizing our dataset.</p>
<p>When we have data that follows a <strong>normal</strong> distribution, we can completely understand our dataset using the <code>mean</code> and <code>standard deviation</code>.</p>
<p>However, if our dataset is <strong>skewed</strong>, the <code>5 number summary</code> (and measures of center associated with it) might be better to summarize our dataset.  </p>
<hr>
<h2 id="outliers">Outliers</h2>
<p>We learned that outliers have a larger influence on measures like the mean than on measures like the median.  We learned that we should work with outliers on a situation by situation basis.  Common techniques include:</p>
<p><strong>1.</strong> At least note they exist and the impact on summary statistics.</p>
<p><strong>2.</strong> If typo - remove or fix</p>
<p><strong>3.</strong> Understand why they exist, and the impact on questions we are trying to answer about our data.</p>
<p><strong>4.</strong> Reporting the 5 number summary values is often a better indication than measures like the mean and standard deviation when we have outliers. </p>
<p><strong>5.</strong> Be careful in reporting. Know how to ask the right questions.</p>
<hr>
<h2 id="histograms-and-box-plots">Histograms and Box Plots</h2>
<p>We also looked at histograms and box plots to visualize our quantitative data.  Identifying outliers and the shape associated with the distribution of our data are easier when using a visual as opposed to using summary statistics.</p>
</div>

<hr>
<div ><h3 id="more-on-center-and-spread">More On Center And Spread</h3>
<p>When analyzing skewed data, it is common to report numeric summaries like the median and 5 number summary, as the mean and standard deviation may be misleading.  </p>
<p>However, with symmetric data, the mean and standard deviation are commonly used, as we can understand what proportion of points might fall 1, 2, or 3 standard deviations away based on the empirical rule associated with normal distributions.</p>
</div></div><span></span></div></div></div><div><div ><p>You can read more about this <a target="_blank" href="https://www.mathsisfun.com/data/standard-normal-distribution.html">here</a>.  </p>
<h3 id="standard-deviation-and-skewed-distributions">Standard Deviation and Skewed Distributions</h3>
<p>Standard Deviations can be calculated for any data set, whether it is normally distributed or skewed. So with the data below be careful what assumptions you are making about the underlying data.</p>
<p>Also the standard deviation basically provides which of two sets of data are more spread out.</p>
</div></div><span></span></div></div></div>
  
  <div ><h2 id="descriptive-vs-inferential-statistics">Descriptive vs. Inferential Statistics</h2>
<p>In this section, we learned about how <strong>Inferential Statistics</strong> differs from <strong>Descriptive Statistics</strong>.  </p>
<hr>
<h3 id="descriptive-statistics">Descriptive Statistics</h3>
<p><code>Descriptive statistics</code> <strong>is about describing our collected data</strong> using the measures discussed throughout this lesson: measures of center, measures of spread, shape of our distribution, and outliers.  We can also use plots of our data to gain a better understanding.</p>
<hr>
<h3 id="inferential-statistics">Inferential Statistics</h3>
<p><code>Inferential Statistics</code> <strong>is about using our collected data to draw conclusions to a larger population</strong>.  Performing inferential statistics well requires that we take a sample that accurately represents our population of interest.  </p>
<p>A common way to collect data is via a survey.  However, surveys may be extremely biased depending on the types of questions that are asked, and the way the questions are asked.   This is a topic you should think about when tackling the first project.  </p>
<p>We looked at specific examples that allowed us to identify the </p>
<ol>
<li><strong>Population</strong> - our entire group of interest.</li>
<li><strong>Parameter</strong> - numeric summary about a population</li>
<li><strong>Sample</strong> - subset of the population</li>
<li><strong>Statistic</strong> - numeric summary about a sample</li>
</ol>
<hr>
</div>

## SQL Aggregation

NULLs are a datatype that specifies where no data exists in SQL.

<div <p> Notice that <strong>NULL</strong>s are different than a zero - they are cells where data does not exist. </p>
<p>When identifying <strong>NULL</strong>s in a <strong>WHERE</strong> clause, we write <strong>IS NULL</strong> or <strong>IS NOT NULL</strong>.  We don't use <code>=</code>, because <strong>NULL</strong> isn't considered a value in SQL.  Rather, it is a property of the data.</p>
<h3 id="nulls-expert-tip">NULLs - Expert Tip</h3>
<p>There are two common ways in which you are likely to encounter <strong>NULL</strong>s:</p>
<ul>
<li><p><strong>NULL</strong>s frequently occur when performing a <strong>LEFT</strong> or <strong>RIGHT JOIN</strong>. You saw in the last lesson - when some rows in the left table of a left join are not matched with rows in the right table, those rows will contain some <strong>NULL</strong> values in the result set.<br><br></p>
</li>
<li><p><strong>NULL</strong>s can also occur from simply missing data in our database.</p>
</li>
</ul>
</div></div></div></div>
<hr>

<div><div ><h3 id="count-the-number-of-rows-in-a-table">COUNT the Number of Rows in a Table</h3>
<p>Try your hand at finding the number of rows in each table.  Here is an example of finding all the rows in the <strong>accounts</strong> table.</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> <span class="hljs-keyword">COUNT</span>(*)
<span class="hljs-keyword">FROM</span> accounts;</span>
</code></pre><p>But we could have just as easily chosen a column to drop into the aggregation function:</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> <span class="hljs-keyword">COUNT</span>(accounts.<span class="hljs-keyword">id</span>)
<span class="hljs-keyword">FROM</span> accounts;</span>
</code></pre><p>These two statements are equivalent, but this isn't always the case.</p>
  <p>Notice that <strong>COUNT</strong> does not consider rows that have <strong>NULL</strong> values.  Therefore, this can be useful for quickly identifying which rows have missing data.</p>
</div></div><span></span></div></div></div>

<p>Functionally, <strong>MIN</strong> and <strong>MAX</strong> are similar to <strong>COUNT</strong> in that they can be used on non-numerical columns. Depending on the column type, <strong>MIN</strong> will return the lowest number, earliest date, or non-numerical value as early in the alphabet as possible. As you might suspect, <strong>MAX</strong> does the opposite—it returns the highest number, the latest date, or the non-numerical value closest alphabetically to “Z.”</p>

<p>Similar to other software <strong>AVG</strong> returns the mean of the data - that is the sum of all of the values in the column divided by the number of values in a column.  This aggregate function again ignores the <strong>NULL</strong> values in both the numerator and the denominator.</p>

<div <p>The key takeaways here:</p>
<ul>
<li><p><strong>GROUP BY</strong> can be used to aggregate data within subsets of the data.  For example, grouping for different accounts, different regions, or different sales representatives.<br><br></p>
</li>
<li><p>Any column in the <strong>SELECT</strong> statement that is not within an aggregator must be in the <strong>GROUP BY</strong> clause.<br><br></p>
</li>
<li><p>The <strong>GROUP BY</strong> always goes between <strong>WHERE</strong> and <strong>ORDER BY</strong>.<br><br></p>
</li>
<li><p><strong>ORDER BY</strong> works like <strong>SORT</strong> in spreadsheet software.</p>
</li>
</ul>
<h3 id="group-by-expert-tip">GROUP BY - Expert Tip</h3>
<p>Before we dive deeper into aggregations using <strong>GROUP BY</strong> statements, it is worth noting that SQL evaluates the aggregations before the <strong>LIMIT</strong> clause. If you don’t group by any columns, you’ll get a 1-row result—no problem there. If you group by a column with enough unique values that it exceeds the <strong>LIMIT</strong> number, the aggregates will be calculated, and then some rows will simply be omitted from the results.</p>
<p>This is actually a nice way to do things because you know you’re going to get the correct aggregates. If SQL cuts the table down to 100 rows, then performed the aggregations, your results would be substantially different. The above query’s results exceed 100 rows, so it’s a perfect example. In the next concept, use the SQL environment to try removing the <strong>LIMIT</strong> and running it again to see what changes.</p>
</div></div></div></div>

<div <p>Key takeaways:</p>
<ul>
<li>You can <strong>GROUP BY</strong> multiple columns at once, as we showed here.  This is often useful to aggregate across a number of different segments.  <br><br></li>
<li>The order of columns listed in the <strong>ORDER BY</strong> clause does make a difference.  You are ordering the columns from left to right.</li>
</ul>
<h3 id="group-by-expert-tips">GROUP BY - Expert Tips</h3>
<ul>
<li><p>The order of column names in your <strong>GROUP BY</strong> clause doesn’t matter—the results will be the same regardless. If we run the same query and reverse the order in the <strong>GROUP BY</strong> clause, you can see we get the same results.<br><br></p>
</li>
<li><p>As with <strong>ORDER BY</strong>, you can substitute numbers for column names in the <strong>GROUP BY</strong> clause. It’s generally recommended to do this only when you’re grouping many columns, or if something else is causing the text in the GROUP BY clause to be excessively long.<br><br></p>
</li>
<li><p>A reminder here that any column that is not within an aggregation must show up in your GROUP BY statement.  If you forget, you will likely get an error.  However, in the off chance that your query does work, you might not like the results! </p>
</li>
</ul>
</div></div></div></div>

<div ><div <p><strong>DISTINCT</strong> is always used in <strong>SELECT</strong> statements, and it provides the unique rows for all columns written in the <strong>SELECT</strong> statement.  Therefore, you only use <strong>DISTINCT</strong> once in any particular <strong>SELECT</strong> statement. </p>
<p>You could write:</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> <span class="hljs-keyword">DISTINCT</span> column1, column2, column3
<span class="hljs-keyword">FROM</span> table1;</span>
</code></pre><p>which would return the unique (or <strong>DISTINCT</strong>) rows across all three columns.</p>
<p>You would <strong>not</strong> write:</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> <span class="hljs-keyword">DISTINCT</span> column1, <span class="hljs-keyword">DISTINCT</span> column2, <span class="hljs-keyword">DISTINCT</span> column3
<span class="hljs-keyword">FROM</span> table1;</span>
</code></pre><p> You can think of <strong>DISTINCT</strong> the same way you might think of the statement "unique".  </p>
<h3 id="distinct-expert-tip">DISTINCT - Expert Tip</h3>
<p>It’s worth noting that using <strong>DISTINCT</strong>, particularly in aggregations, can slow your queries down quite a bit. </p>
</div></div></div></div></div>

<div ><h3 id="having-expert-tip">HAVING - Expert Tip</h3>
<p><strong>HAVING</strong> is the “clean” way to filter a query that has been aggregated, but this is also commonly done using a <a target="_blank" href="https://community.modeanalytics.com/sql/tutorial/sql-subqueries/">subquery</a>.  Essentially, any time you want to perform a <strong>WHERE</strong> on an element of your query that was created by an aggregate, you need to use <strong>HAVING</strong> instead.</p>
</div>

<div <p><strong>GROUP</strong>ing <strong>BY</strong> a date column is not usually very useful in SQL, as these columns tend to have transaction data down to a second.  Keeping date information at such a granular data is both a blessing and a curse, as it gives really precise information (a blessing), but it makes grouping information together directly difficult (a curse).  </p>
<p>Lucky for us, there are a number of built in SQL functions that are aimed at helping us improve our experience in working with dates.</p>
<p><strong>Here we saw that dates are stored in year, month, day, hour, minute, second, which helps us in truncating.  In the next concept, you will see a number of functions we can use in SQL to take advantage of this functionality.</strong></p>
<p>In <a target="_blank" href="https://en.wikipedia.org/wiki/Date_format_by_country">this link you can find the formatting of dates around the world, as referenced in the video</a>.</p>
</div></div></div></div>

<div <p>The first function you are introduced to in working with dates is <strong>DATE_TRUNC</strong>.</p>
<p><strong>DATE_TRUNC</strong> allows you to truncate your date to a particular part of your date-time column.  Common trunctions are <code>day</code>, <code>month</code>, and <code>year</code>.  <a target="_blank" href="https://blog.modeanalytics.com/date-trunc-sql-timestamp-function-count-on/">Here</a> is a great blog post by Mode Analytics on the power of this function. </p>
<p><strong>DATE_PART</strong> can be useful for pulling a specific portion of a date, but notice pulling <code>month</code> or day of the week (<code>dow</code>) means that you are no longer keeping the years in order.  Rather you are grouping for certain components regardless of which year they belonged in.</p>
<p>For additional functions you can use with dates, check out the documentation <a target="_blank" href="https://www.postgresql.org/docs/9.1/static/functions-datetime.html">here</a>, but the <strong>DATE_TRUNC</strong> and <strong>DATE_PART</strong> functions definitely give you a great start!</p>
<p>You can reference the columns in your select statement in <strong>GROUP BY</strong> and <strong>ORDER BY</strong> clauses with numbers that follow the order they appear in the select statement. For example</p>
<p>SELECT standard_qty, COUNT(*)</p>
<p>FROM orders</p>
<p>GROUP BY 1   <em>(this 1 refers to standard_qty since it is the first of the columns included in the select statement)</em></p>
<p>ORDER BY 1    <em>(this 1 refers to standard_qty since it is the first of the columns included in the select statement)</em></p>
</div></div></div></div>

<div ><h3 id="case-expert-tip">CASE - Expert Tip</h3>
<ul>
<li>The CASE statement always goes in the SELECT clause.<br><br></li>
<li>CASE must include the following components: WHEN, THEN, and END. ELSE is an optional component to catch cases that didn’t meet any of the other previous CASE conditions.<br><br></li>
<li>You can make any conditional statement using any conditional operator (like <a target="_blank" href="https://mode.com/resources/sql-tutorial/sql-where">WHERE</a>) between WHEN and THEN. This includes stringing together multiple conditional statements using AND and OR.<br><br></li>
<li>You can include multiple WHEN statements, as well as an ELSE statement again, to deal with any unaddressed conditions.</li>
</ul>
<p> Example</p>
  
```sql
SELECT OrderID, Quantity,
CASE
    WHEN Quantity > 30 THEN "The quantity is greater than 30"
    WHEN Quantity = 30 THEN "The quantity is 30"
    ELSE "The quantity is under 30"
END AS QuantityText
FROM OrderDetails;
```

</div>


<div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h1 id="subquery-formatting">Subquery Formatting</h1>
<p>When writing <strong>Subqueries</strong>, it is easy for your query to look incredibly complex.  In order to assist your reader, which is often just yourself at a future date, formatting SQL will help with understanding your code.  </p>
<p>The important thing to remember when using subqueries is to provide some way for the reader to easily determine which parts of the query will be executed together. Most people do this by indenting the subquery in some way - you saw this with the solution blocks in the previous concept.  </p>
<p>The examples in this class are indented quite far—all the way to the parentheses. This isn’t practical if you nest many subqueries, but in general, be thinking about how to write your queries in a readable way.  Examples of the same query written multiple different ways is provided below.  You will see that some are much easier to read than others.</p>
<hr>
<h3 id="badly-formatted-queries">Badly Formatted Queries</h3>
<p>Though these poorly formatted examples will execute the same way as the well formatted examples, they just aren't very friendly for understanding what is happening!</p>
<p>Here is the first, where it is impossible to decipher what is going on:</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> * <span class="hljs-keyword">FROM</span> (<span class="hljs-keyword">SELECT</span> DATE_TRUNC(<span class="hljs-string">'day'</span>,occurred_at) <span class="hljs-keyword">AS</span> <span class="hljs-keyword">day</span>, channel, <span class="hljs-keyword">COUNT</span>(*) <span class="hljs-keyword">as</span> <span class="hljs-keyword">events</span> <span class="hljs-keyword">FROM</span> web_events <span class="hljs-keyword">GROUP</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">1</span>,<span class="hljs-number">2</span> <span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">3</span> <span class="hljs-keyword">DESC</span>) sub;</span>
</code></pre><p>This second version, which includes some helpful line breaks, is easier to read than that previous version, but it is still not as easy to read as the queries in the <strong>Well Formatted Query</strong> section.</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> *
<span class="hljs-keyword">FROM</span> (
<span class="hljs-keyword">SELECT</span> DATE_TRUNC(<span class="hljs-string">'day'</span>,occurred_at) <span class="hljs-keyword">AS</span> <span class="hljs-keyword">day</span>,
channel, <span class="hljs-keyword">COUNT</span>(*) <span class="hljs-keyword">as</span> <span class="hljs-keyword">events</span>
<span class="hljs-keyword">FROM</span> web_events 
<span class="hljs-keyword">GROUP</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">1</span>,<span class="hljs-number">2</span>
<span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">3</span> <span class="hljs-keyword">DESC</span>) sub;</span>
</code></pre><hr>
<h3 id="well-formatted-query">Well Formatted Query</h3>
<p>Now for a well formatted example, you can see the table we are pulling from much easier than in the previous queries.  </p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> *
<span class="hljs-keyword">FROM</span> (<span class="hljs-keyword">SELECT</span> DATE_TRUNC(<span class="hljs-string">'day'</span>,occurred_at) <span class="hljs-keyword">AS</span> <span class="hljs-keyword">day</span>,
                channel, <span class="hljs-keyword">COUNT</span>(*) <span class="hljs-keyword">as</span> <span class="hljs-keyword">events</span>
      <span class="hljs-keyword">FROM</span> web_events 
      <span class="hljs-keyword">GROUP</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">1</span>,<span class="hljs-number">2</span>
      <span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">3</span> <span class="hljs-keyword">DESC</span>) sub;</span>
</code></pre><p>Additionally, if we have a <strong>GROUP BY</strong>, <strong>ORDER BY</strong>, <strong>WHERE</strong>, <strong>HAVING</strong>, or any other statement following our subquery, we would then indent it at the same level as our outer query.</p>
<p>The query below is similar to the above, but it is applying additional statements to the outer query, so you can see there are <strong>GROUP BY</strong> and <strong>ORDER BY</strong> statements used on the output are not tabbed. The inner query <strong>GROUP BY</strong> and <strong>ORDER BY</strong> statements are indented to match the inner table.</p>
<pre><code><span class="hljs-operator"><span class="hljs-keyword">SELECT</span> *
<span class="hljs-keyword">FROM</span> (<span class="hljs-keyword">SELECT</span> DATE_TRUNC(<span class="hljs-string">'day'</span>,occurred_at) <span class="hljs-keyword">AS</span> <span class="hljs-keyword">day</span>,
                channel, <span class="hljs-keyword">COUNT</span>(*) <span class="hljs-keyword">as</span> <span class="hljs-keyword">events</span>
      <span class="hljs-keyword">FROM</span> web_events 
      <span class="hljs-keyword">GROUP</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">1</span>,<span class="hljs-number">2</span>
      <span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">3</span> <span class="hljs-keyword">DESC</span>) sub
<span class="hljs-keyword">GROUP</span> <span class="hljs-keyword">BY</span> <span class="hljs-keyword">day</span>, channel, <span class="hljs-keyword">events</span>
<span class="hljs-keyword">ORDER</span> <span class="hljs-keyword">BY</span> <span class="hljs-number">2</span> <span class="hljs-keyword">DESC</span>;</span>
</code></pre><p>These final two queries are so much easier to read!</p>
</div></div><span></span></div>

<hr>

<div><div class="index--container--2OwOl"><div class="index--atom--lmAIo layout--content--3Smmq"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h3 id="subqueries-part-ii">Subqueries Part II</h3>
<p>In the first subquery you wrote, you created a table that you could then query again in the <strong>FROM</strong> statement.  However, if you are only returning a single value, you might use that value in a logical statement like <strong>WHERE</strong>, <strong>HAVING</strong>, or even <strong>SELECT</strong> - the value could be nested within a <strong>CASE</strong> statement.  </p>
<p>On the next concept, we will work through this example, and then you will get some practice on answering some questions on your own.</p>
</div></div><span></span></div></div></div>

<hr>

<div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>The <strong>WITH</strong> statement is often called a <strong>Common Table Expression</strong> or <strong>CTE</strong>.  Though these expressions serve the exact same purpose as subqueries, they are more common in practice, as they tend to be cleaner for a future reader to follow the logic.  </p>
<p>In the next concept, we will walk through this example a bit more slowly to make sure you have all the similarities between subqueries and these expressions down for you to use in practice!  If you are already feeling comfortable skip ahead to practice the quiz section.</p>
</div></div>

**Example**

<pre><code>WITH table1 AS (
          <span class="hljs-operator"><span class="hljs-keyword">SELECT</span> *
          <span class="hljs-keyword">FROM</span> web_events),

     table2 <span class="hljs-keyword">AS</span> (
          <span class="hljs-keyword">SELECT</span> *
          <span class="hljs-keyword">FROM</span> accounts)


<span class="hljs-keyword">SELECT</span> *
<span class="hljs-keyword">FROM</span> table1
<span class="hljs-keyword">JOIN</span> table2
<span class="hljs-keyword">ON</span> table1.account_id = table2.<span class="hljs-keyword">id</span>;</span>
</code></pre>

<hr>

<div class="_notes-wide--notes-wide--23TbE"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>Here we looked at three new functions:</p>
<ol>
<li><strong>LEFT</strong></li>
<li><strong>RIGHT</strong></li>
<li><strong>LENGTH</strong></li>
</ol>
<p><strong>LEFT</strong> pulls a specified number of characters for each row in a specified column starting at the beginning (or from the left).  As you saw here, you can pull the first three digits of a phone number using <strong>LEFT(phone_number, 3)</strong>.<br><br></p>
<p><strong>RIGHT</strong> pulls a specified number of characters for each row in a specified column starting at the end (or from the right).  As you saw here, you can pull the last eight digits of a phone number using <strong>RIGHT(phone_number, 8)</strong>.<br><br></p>
<p><strong>LENGTH</strong> provides the number of characters for each row of a specified column.  Here, you saw that we could use this to get the length of each phone number as <strong>LENGTH(phone_number)</strong>.</p>
</div></div></div>

<hr>

<div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>In this lesson, you learned about:</p>
<ol>
<li><strong>POSITION</strong></li>
<li><strong>STRPOS</strong></li>
<li><strong>LOWER</strong></li>
<li><strong>UPPER</strong></li>
</ol>
<p><strong>POSITION</strong> takes a character and a column, and provides the index where that character is for each row.  The index of the first position is 1 in SQL.  If you come from another programming language, many begin indexing at 0.  Here, you saw that you can pull the index of a comma as <strong>POSITION(',' IN city_state)</strong>.<br><br></p>
<p><strong>STRPOS</strong> provides the same result as <strong>POSITION</strong>, but the syntax for achieving those results is a bit different as shown here: <strong>STRPOS(city_state, ',')</strong>.<br><br></p>
<p>Note, both <strong>POSITION</strong> and <strong>STRPOS</strong> are case sensitive, so looking for <strong>A</strong> is different than looking for <strong>a</strong>.  <br><br></p>
<p>Therefore, if you want to pull an index regardless of the case of a letter, you might want to use <strong>LOWER</strong> or <strong>UPPER</strong> to make all of the characters lower or uppercase.</p>
</div></div>

<hr>

<div class="index--instructor-notes-wide--6JxNO layout--content-wide--tivIS layout--content--3Smmq"><div class="_notes-wide--notes-wide--23TbE"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><p>In this lesson you learned about:</p>
<ol>
<li><strong>CONCAT</strong></li>
<li>Piping <code>||</code></li>
</ol>
<p>Each of these will allow you to combine columns together across rows.  In this video, you saw how first and last names stored in separate columns could be combined together to create a full name: <strong>CONCAT(first_name, ' ', last_name)</strong> or with piping as <strong>first_name || ' ' || last_name</strong>.</p>
</div></div></div></div>

<hr>

<div class="index-module--markdown--2MdcR ureact-markdown "><p>In this video, you saw additional functionality for working with dates including:</p>
<ol>
<li><strong>TO_DATE</strong></li>
<li><strong>CAST</strong></li>
<li>Casting with <code>::</code></li>
</ol>
<p><strong>DATE_PART('month', TO_DATE(month, 'month'))</strong> here changed a month name into the number associated with that particular month.<br><br></p>
<p>Then you can change a string to a date using <strong>CAST</strong>.  <strong>CAST</strong> is actually useful to change lots of column types.  Commonly you might be doing as you saw here, where you change a <code>string</code> to a <code>date</code> using <strong>CAST(date_column AS DATE)</strong>.  However, you might want to make other changes to your columns in terms of their data types.  You can see other examples <a target="_blank" href="http://www.postgresqltutorial.com/postgresql-cast/">here</a>.</p>
<p>In this example, you also saw that instead of <strong>CAST(date_column AS DATE)</strong>, you can use <strong>date_column::DATE</strong>.</p>
<h3 id="expert-tip">Expert Tip</h3>
<p>Most of the functions presented in this lesson are specific to strings.  They won’t work with dates, integers or floating-point numbers. However, using any of these functions will automatically change the data to the appropriate type. </p>
<p><strong>LEFT</strong>, <strong>RIGHT</strong>, and <strong>TRIM</strong> are all used to select only certain elements of strings, but using them to select elements of a number or date will treat them as strings for the purpose of the function.  Though we didn't cover <strong>TRIM</strong> in this lesson explicitly, it can be used to remove characters from the beginning and end of a string.  This can remove unwanted spaces at the beginning or end of a row that often happen with data being moved from Excel or other storage systems.</p>
<p>There are a number of variations of these functions, as well as several other string functions not covered here. 
 Different databases use subtle variations on these functions, so be sure to look up the appropriate database’s syntax if you’re connected to a private database.The <a target="_blank" href="http://www.postgresql.org/docs/9.1/static/functions-string.html">Postgres literature</a> contains a lot of the related functions.</p>
</div>

<hr>

<p>In this video, you learned about how to use <strong>COALESCE</strong> to work with NULL values.  Unfortunately, our dataset does not have the <strong>NULL</strong> values that were fabricated in this dataset, so you will work through a different example in the next concept to get used to the <strong>COALESCE</strong> function.</p>

<hr>

<div class="index-module--markdown--2MdcR ureact-markdown "><p>For quantitative data, if we are just looking at one column worth of data, we have four common visuals:</p>
<ol>
<li>Histogram</li>
<li>Normal Quantile Plot</li>
<li>Stem and Leaf Plot</li>
<li>Box and Whisker Plot</li>
</ol>
<p>In most cases, you will want to use a <strong>histogram</strong>.</p>
<p>For categorical data, if we are looking at just one variable (column), we have three common visuals:</p>
<ol>
<li>Bar Chart</li>
<li>Pie Chart</li>
<li>Pareto Chart</li>
</ol>
<p>In most cases, you will want to use a <strong>bar chart</strong>.</p>
</div>

<hr>

<div class="index--instructor-notes-wide--6JxNO layout--content-wide--tivIS layout--content--3Smmq"><div class="_notes-wide--notes-wide--23TbE"><div class="ltr"><div class="index-module--markdown--2MdcR ureact-markdown "><h3 id="scatter-plots">Scatter plots</h3>
<p>Scatter plots are a common visual for comparing two quantitative variables.  A common summary statistic that relates to a scatter plot is the <strong>correlation coefficient</strong> commonly denoted by <strong>r</strong>.</p>
<p>Though there are a <a target="_blank" href="http://www.statisticssolutions.com/correlation-pearson-kendall-spearman/">few different ways</a> to measure correlation between two variables, the most common way is with <a target="_blank" href="https://en.wikipedia.org/wiki/Pearson_correlation_coefficient">Pearson's correlation coefficient</a>.  Pearson's correlation coefficient provides the:</p>
<ol>
<li>Strength</li>
<li>Direction</li>
</ol>
<p>of a <strong>linear relationship</strong>.  <a target="_blank" href="https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient">Spearman's Correlation Coefficient</a> does not measure linear relationships specifically, and it might be more appropriate for certain cases of associating two variables.</p>
</div></div></div></div>

<hr>

<a href="https://ibb.co/7jGnczj"><img src="https://i.ibb.co/Kb92ZGb/image.png" alt="image" border="0"></a>

<hr>

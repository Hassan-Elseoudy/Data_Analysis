# Data Analysis

## What is Data Analysis?
#### 1. Questions
Either you're given data and ask questions based on it, or you ask questions first and gather data based on that later.
In both cases, great questions help you focus on relevant parts of your data and direct your analysis towards meaningful
insights.

#### 2. Wrangle
You get the data you need in a form you can work with in three steps: **gather, assess, clean**. You gather the data you
need to answer your questions, assess your data to identify any problems in your data’s quality or structure, and clean
your data by **modifying, replacing, or removing data** to ensure that your dataset is of the highest quality and as
well-structured as possible.

#### 3. Perform EDA (Exploratory Data Analysis)
You explore and then augment your data to maximize the potential of your analyses, visualizations, and models. Exploring
involves **finding patterns in your data, visualizing relationships in your data, and building intuition about what
you’re working with.** After exploring, you can do things like **remove outliers and create better features from your
data**, also known as feature engineering.

#### 4. Draw Conclusions
This step is typically approached with machine learning or inferential statistics.

#### 5. Communicate
You often need to justify and convey meaning in the insights you’ve found. Or, if your end goal is to build a system,
you usually need to share what you’ve built, explain how you reached design decisions, and report how well it performs.
There are many ways to communicate your results: reports, slide decks, blog posts, emails, presentations, or even
conversations. Data visualization will always be very valuable.
<hr>
<h2>Descriptive Statistics I</h2>
<p>The table below summarizes our data types.</p>
<table>
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
      <td>Pages in a Book, Trees in Yard, Dogs at a Coffee Shop</td>
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
      <td>Letter Grade, Survey Rating</td>
      <td>Gender, Marital Status, Breakfast Items</td>
    </tr>
  </tbody>
</table>

<h3> Quantitative vs. Categorical</h3>
<p>Some of these can be a bit tricky - notice even though zip codes are a number, they aren’t really a quantitative
  variable. If we add two zip codes together, we do not obtain any useful information from this new value. Therefore,
  this is a categorical variable. </p>
<p><strong>Height</strong>, <strong>Age</strong>, the <strong>Number of Pages in a Book</strong> and <strong>Annual
    Income</strong> all take on values that we can add, subtract and perform other operations with to gain useful
  insight. Hence, these are <code>quantitative</code>. </p>
<p><strong>Gender</strong>, <strong>Letter Grade</strong>, <strong>Breakfast Type</strong>, <strong>Marital
    Status</strong>, and <strong>Zip Code</strong> can be thought of as labels for a group of items or individuals.
  Hence, these are <code>categorical</code>.</p>

<h3>Continuous vs. Discrete</h3>
<p>To consider if we have continuous or discrete data, we should see if we can split our data into smaller and smaller
  units. Consider time - we could measure an event in years, months, days, hours, minutes, or seconds, and even at
  seconds we know there are smaller units we could measure time in. Therefore, we know this data type is
  <code>continuous</code>. <strong>Height</strong>, <strong>age</strong>, and <strong>income</strong> are all examples
  of <code>continuous data</code>. Alternatively, or <strong>trees in a yard</strong> are <code>discrete data</code>.
</p>

<h3>Ordinal vs. Nominal</h3>
<p>In looking at categorical variables, we found <strong>Gender</strong>, <strong>Marital Status</strong>, <strong>Zip
    Code</strong> and your <strong>Breakfast items</strong> are <code>nominal variables</code> where there is no order
  ranking associated with this type of data. Whether you ate cereal, toast, eggs, or only coffee for breakfast; there
  is no rank ordering associated with your breakfast. </p>
<p>Alternatively, the <strong>Letter Grade</strong> or <strong>Survey Ratings</strong> have a rank ordering associated
  with it, as <code>ordinal data</code>. If you receive an A, this is higher than an A-. An A- is ranked higher than a
  B+, and so on... Ordinal variables frequently occur on rating scales from very poor to very good.</p>

<h2>Analyzing Quantitative Data</h2>
<h4>Four Aspects for Quantitative Data</h4>
<p>There are four main aspects to analyzing <strong>Quantitative</strong> data. </p>
<ol>
  <li>Measures of <code>Center</code></li>
  <li>Measures of <code>Spread</code></li>
  <li>The <code>Shape</code> of the data.</li>
  <li><code>Outliers</code></li>
</ol>
<h4>Analyzing Categorical Data</h4>
<p>Analyzing categorical data has fewer parts to consider. <strong>Categorical</strong> data is analyzed usually by
  looking at the counts or proportion of individuals that fall into each group. For example if we were looking at the
  breeds of the dogs, we would care about how many dogs are of each breed, or what proportion of dogs are of each breed
  type.</p>
<h3>Measures of Center</h3>
<p>There are three measures of center:</p>
<ol>
  <li><code>Mean</code></li>
  <li><code>Median</code></li>
  <li><code>Mode</code></li>
</ol>
<h3>The Mean</h3>
<p>The mean is often called the average or the <strong>expected value</strong> in mathematics. We calculate the mean by
  adding all of our values together, and dividing by the number of values in our dataset.</p>

<h3>The Median</h3>
<p>The <strong>median</strong> splits our data so that 50% of our values are lower and 50% are higher. We found how we
  calculate the median depends on if we have an even number of observations or an odd number of observations. </p>
<h4>- Median for Odd Values</h4>
<p>If we have an <strong>odd</strong> number of observations, the <strong>median</strong> is simply the number in the
  <strong>direct middle</strong>. For example, if we have 7 observations, the median is the fourth value when our
  numbers are ordered from smallest to largest. If we have 9 observations, the median is the fifth value. </p>
<h4>- Median for Even Values</h4>
<p>If we have an <strong>even</strong> number of observations, the <strong>median</strong> is the <strong>average of the
    two values in the middle</strong>. For example, if we have 8 observations, we average the fourth and fifth values
  together when our numbers are ordered from smallest to largest. </p>
<p>In order to compute the median we <b>MUST</b> sort our values first. </p>
<p>Whether we use the mean or median to describe a dataset is largely dependent on the <strong>shape</strong> of our
  dataset and if there are any <strong>outliers</strong>.</p>

<h3>The Mode</h3>
<p>The <strong>mode</strong> is the most frequently observed value in our dataset. </p>
<p>There might be multiple modes for a particular dataset, or no mode at all. </p>
<h4>- No Mode</h4>
<p>If all observations in our dataset are observed with the same frequency, there is no mode. If we have the dataset:
</p>
<p>1, 1, 2, 2, 3, 3, 4, 4</p>
<p>There is <b>no mode</b>, because all observations occur the same number of times. </p>
<h4>- Many Modes</h4>
<p>If two (or more) numbers share the maximum value, then there is more than one mode. If we have the dataset:</p>
<p>1, 2, 3, 3, 3, 4, 5, 6, 6, 6, 7, 8, 9 </p>
<p>There are two modes 3 and 6, because these values share the maximum frequencies at 3 times, while all other values
  only appear once. </p>

<h2>Notation</h2>
<p>Notation is a common language used to communicate mathematical ideas. <strong>Think of notation as a universal
    language used by academic and industry professionals to convey mathematical ideas.</strong></p>
<p>You likely already know some notation. Plus, minus, multiply, division, and equal signs all have mathematical symbols
  that you are likely familiar with. Each of these symbols replaces an idea for how numbers interact with one another.
  it does have the following properties:</p>
<ol>
  <li>
    <p><strong>Understanding how to correctly use notation makes you seem really smart.</strong> Knowing how to read and
      write in notation is like learning a new language. A language that is used to convey ideas associated with
      mathematics. <br><br></p>
  </li>
  <li>
    <p><strong>It allows you to read documentation, and implement an idea to your own problem.</strong> Notation is used
      to convey how problems are solved all the time. One really popular mathematical algorithm that is used to solve
      some of the world's most difficult problems is known as Gradient Boosting. The way that it solves problems is
      explained here: <a target="_blank"
        href="https://en.wikipedia.org/wiki/Gradient_boosting">https://en.wikipedia.org/wiki/Gradient_boosting</a>. If
      you really want to understand how this algorithm works, you need to be able to read and understand notation. </p>
  </li>
  <li>
    <p><strong>It makes ideas that are hard to say in words easier to convey.</strong></p>
  </li>
</ol>

<h3>Example to Introduce Notation</h3>
<h4>Rows and Columns</h4>
<p>Spreadsheets are a common way to hold data. They are composed of rows and columns. Rows run horizontally, while
  columns run vertically. Each column in a spreadsheet commonly holds a specific <strong>variable</strong>, while each
  row is commonly called an <strong>instance</strong> or <strong>individual</strong>. </p>
<table>
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
<p>This is a <strong>row</strong>:</p>
<table>
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
<p>This is a <strong>column</strong>:</p>
<table>
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
<h4>Before Collecting Data</h4>
<p><strong>Before collecting data, we usually start with a question, or many questions, that we would like to answer.
    The purpose of data is to help us in answering these questions.</strong></p>
<h4>Random Variables</h4>
<p>A <strong>random variable</strong> is a placeholder for the possible values of some process (mostly... the term 'some
  process' is a bit ambiguous). As was stated before, notation is useful in that it helps us take complex ideas and
  simplify (often to a single letter or single symbol). We see random variables represented by capital letters
  (<strong>X</strong>, <strong>Y</strong>, or <strong>Z</strong> are common ways to represent a random variable). </p>
<p>We might have the random variable <strong>X</strong>, which is a holder for the possible values of the amount of time
  someone spends on our site. Or the random variable <strong>Y</strong>, which is a holder for the possible values of
  whether or not an individual purchases a product. </p>
<p><strong>X</strong> is 'a holder' of the values that could possibly occur for the amount of time spent on our website.
  Any number from 0 to infinity really. </p>

<h3>Capital vs. Lower Case Letters</h3>
<p><strong>Random variables</strong> are represented by capital letters. Once we observe an outcome of these random
  variables, we notate it as a lower case of the same letter. </p>
<h4>Example 1</h4>
<p>For example, the <strong>amount of time someone spends on our site</strong> is a <strong>random variable</strong> (we
  are not sure what the outcome will be for any particular visitor), and we would notate this with <strong>X</strong>.
  Then when the first person visits the website, if they spend 5 minutes, we have now observed this outcome of our
  random variable. We would notate any outcome as a lowercase letter with a subscript associated with the order that we
  observed the outcome. </p>
<p>If 5 individuals visit our website, the first spends 10 minutes, the second spends 20 minutes, the third spends 45
  mins, the fourth spends 12 minutes, and the fifth spends 8 minutes; we can notate this problem in the following way:
</p>
<p><strong>X</strong> is the amount of time an individual spends on the website.</p>
<p><b>x<sub>1</sub></b> = 10, <b>x<sub>2</sub></b> = 20, <b>x<sub>3</sub></b> = 45, <b>x<sub>4</sub></b> = 12,
  <b>x<sub>5</sub></b> = 8.</p>
<p>The capital <strong>X</strong> is associated with this idea of a <strong>random variable</strong>, while the
  observations of the random variable take on lowercase <strong>x</strong> values. </p>
<h4>Example 2</h4>
<p>Taking this one step further, we could ask: </p>
<p><strong>What is the probability someone spends more than 20 minutes in our website?</strong></p>
<p>In notation, we would write:</p>
<p><strong>P(X &gt; 20)?</strong></p>
<p>Here <strong>P</strong> stands for <strong>probability</strong>, while the parentheses encompass the statement for
  which we would like to find the probability. Since <strong>X</strong> represents the amount of time spent on the
  website, this notation represents the probability the amount of time on the website is greater than 20. </p>

<h3>Notation for Calculating the Mean</h3>
<p>We know that the mean is calculated as the sum of all our values divided by the number of values in our dataset. </p>
<p>In our current notation, adding all of our values together can be extremely tedious. If we want to add 3 values of
  some random variable together, we would use the notation:</p>
<p><b>x<sub>1</sub></b> + <b>x<sub>2</sub></b> + <b>x<sub>3</sub></b></p>
<p>If we want to add 6 values together, we would use the notation:</p>
<p><b>x<sub>1</sub></b> + <b>x<sub>2</sub></b> + <b>x<sub>3</sub></b> + <b>x<sub>4</sub></b> + <b>x<sub>5</sub></b> +
  <b>x<sub>6</sub></b></p>
<p>To extend this to add one hundred, one thousand, or one million values would be ridiculous! How can we make this
  easier to communicate?!</p>

<h2>Aggregations</h2>

An **aggregation** is a way to turn multiple numbers into fewer numbers (commonly one number).

**Summation** is a common aggregation. The notation used to sum our values is a greek symbol called sigma **Σ**.

#### Example 1

Imagine we are looking at the amount of time individuals spend on our website. We collect data from nine individuals:
If we want to sum the **first three values** together In our new notation, we can write:

<img src='https://latex.codecogs.com/gif.latex?%5Csum_%7Bi%3D1%7D%5E%7Bi%3D3%7Dx_%7Bi%7D'>

#### Other Aggregations

The **Σ** sign is used for aggregating using summation, but we might choose to aggregate in other ways. Summing is one
of the most common ways to need to aggregate. However, we might need to aggregate in alternative ways. If we wanted to
multiply all of our values together we would use a product sign **Π** , capital Greek letter `pi`. The way we aggregate
continuous values is with something known as integration (a common technique in calculus), which uses the following
symbol **∫**


<h2>Final Steps for Calculating the Mean</h2>
<p>To finalize our calculation of the mean, we introduce <strong>n</strong> as the total number of values in our
  dataset. We can use this notation both at the top of our summation, as well as for the value that we divide by when
  calculating the mean. </p>

<img src='https://latex.codecogs.com/gif.latex?%5Cfrac%7B1%7D%7Bn%7D%5Csum_%7Bi%3D1%7D%5E%7Bi%3Dn%7Dx_%7Bi%7D'>
<p>Instead of writing out all of the above, we commonly write <b>x̄</b> to represent the mean of a dataset.
  <hr>
  <h2>Basic SQL</h2>
  <h3>Entity Relationship Diagrams</h3>
  <p>An <strong>entity relationship diagram</strong> (ERD) is a common way to view data in a database. These diagrams
    help you visualize the data you are analyzing including:</p>
  <ol>
    <li>The names of the tables.</li>
    <li>The columns in each table.</li>
    <li>The way the tables work together. </li>
  </ol>

  <h2>Introduction</h2>
  <p>Before we dive into writing Structured Query Language (SQL) queries, let's take a look at what makes SQL and the
    databases that utilize SQL so popular. </p>
  <p>It is an important distinction to say that SQL is a <strong>language</strong>. Hence, the last word of
    SQ<strong>L</strong> being <strong>language</strong>. SQL is most popular for its interaction with databases.</p>

  <h2>Why Do Data Analysts Use SQL?</h2>
  <p>There are some major advantages to using <strong>traditional relational databases,</strong> which we interact
    with using SQL. The five most apparent are:</p>
  <ul>
    <li>SQL is easy to understand.</li>
    <li>Traditional databases allow us to access data directly.</li>
    <li>Traditional databases allow us to audit and replicate our data.</li>
    <li>SQL is a great tool for analyzing multiple tables at once.</li>
    <li>SQL allows you to analyze more complex questions than dashboard tools like Google Analytics.</li>
  </ul>

  <h2>Why Do Businesses Choose SQL?</h2>
  <ol>
    <li>
      <p><strong>Data integrity is ensured</strong> - only the data you want entered is entered, and only certain users
        are able to enter data into the database. <br><br></p>
    </li>
    <li>
      <p><strong>Data can be accessed quickly</strong> - SQL allows you to obtain results very quickly from the data
        stored in a database. Code can be optimized to quickly pull results. <br><br></p>
    </li>
    <li>
      <p><strong>Data is easily shared</strong> - multiple individuals can access data stored in a database, and the
        data is the same for all users allowing for consistent results for anyone with access to your database.</p>
    </li>
  </ol>

  <p>A few key points about data stored in SQL databases:
  </p>
  <ol>
    <li>
      <p><strong>Data in databases is stored in tables that can be thought of just like Excel spreadsheets.</strong>
      </p>
    </li>
    <li>
      <p><strong>All the data in the same column must match in terms of data type. </strong> <br>An entire column is
        considered quantitative, discrete, or as some sort of string. This means if you have one row with a string in a
        particular column, the entire column might change to a text data type. <strong>This can be very bad if you want
          to
          do math with this column!</strong><br><br></p>
    </li>
    <li>
      <p><strong>Consistent column types are one of the main reasons working with databases is fast.</strong> <br>Often
        databases hold <strong>a LOT</strong> of data. So, knowing that the columns are all of the same type of data
        means
        that obtaining data from a database can still be fast.<br><br></p>
    </li>
  </ol>

  ## SQL Basic Statements
  <table>
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
        <td>Orders table based on the column. Used with <strong>DESC</strong>.</td>
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

  <h3>Primary and Foreign Keys</h3>
  <p><strong>JOIN</strong>ing tables in a database has to do with primary and foreign keys:</p>
  <ul>
    <li>
      <p><strong>primary keys</strong> - are unique for every row in a table. These are generally the first column in
        our
        database.</p>
    </li>
    <li>
      <p><strong>foreign keys</strong> - are the <strong>primary key</strong> appearing in another table, which allows
        the
        rows to be non-unique. </p>
    </li>
  </ul>
  <p>Choosing the set up of data in our database is very important, but not usually the job of a data analyst. This
    process is known as <strong>Database Normalization</strong>.</p>
  <h3>JOINs</h3>
  <p>The three <strong>JOIN</strong> statements you are most likely to use are:</p>
  <ol>
    <li><strong>JOIN</strong> - an <strong>INNER JOIN</strong> that only pulls data that exists in both tables.</li>
    <li><strong>LEFT JOIN</strong> - pulls all the data that exists in both tables, as well as all of the rows from the
      table in the <strong>FROM</strong> even if they do not exist in the <strong>JOIN</strong> statement.</li>
    <li><strong>RIGHT JOIN</strong> - pulls all the data that exists in both tables, as well as all of the rows from the
      table in the <strong>JOIN</strong> even if they do not exist in the <strong>FROM</strong> statement.</li>
  </ol>
  <p>There are a few more advanced <strong>JOIN</strong>s that we did not cover here, and they are used in very specific
    use cases. <a target="_blank" href="https://www.w3schools.com/sql/sql_union.asp">UNION and UNION ALL</a>, <a
      target="_blank" href="http://www.w3resource.com/sql/joins/cross-join.php">CROSS JOIN</a>, and the tricky <a
      target="_blank" href="https://www.w3schools.com/sql/sql_join_self.asp">SELF JOIN</a>.</p>

  <h3>Alias</h3>
  <p>This allows to be more efficient in the number of characters needed to write.</p>
  <hr>

  <h2>Descriptive Statistics II</h2>
  <h2>Measures of Spread</h2>
  <p><strong>Measures of Spread</strong> are used to provide us an idea of how spread out our data are from one another.
    Common measures of spread include:</p>
  <ol>
    <li><strong>Range</strong></li>
    <li><strong>Interquartile Range (IQR)</strong></li>
    <li><strong>Standard Deviation</strong></li>
    <li><strong>Variance</strong></li>
  </ol>

  <h2> Histograms</h2>
  <p> Histograms are super useful to understanding the different aspects of quantitative data.</p>
  <h2>Calculating the 5 Number Summary</h2>
  <p>The five number summary consist of 5 values:</p>
  <ol>
    <li><strong>Minimum:</strong> The smallest number in the dataset.</li>
    <li><b>Q<sub>1</sub></b>: The value such that 25% of the data fall below.</li>
    <li><b>Q<sub>2</sub></b>: The value such that 50% of the data fall below.</li>
    <li><b>Q<sub>3</sub></b>: The value such that 75% of the data fall below.</li>
    <li><strong>Maximum:</strong> The largest value in the dataset.</li>
  </ol>
  <h2>Range</h2>
  <p>The <strong>range</strong> is then calculated as the difference between the <strong>maximum</strong> and the
    <strong>minimum</strong>. </p>
  <h2>IQR</h2>
  <p>The <strong>interquartile range</strong> is calculated as the difference between <b>Q<sub>3</sub></b> and
    <b>Q<sub>1</sub></b>
    <h3>Standard Deviation and Variance</h3>
    <p>The <strong>standard deviation</strong> is one of the most common measures for talking about the spread of
      data. It is defined as <strong>the average distance of each observation from the mean</strong>. </p>


    <h2>Shape</h2>
    <p>The distribution of our data is frequently associated with one of the three <strong>shapes</strong>:</p>
    <p><strong>1. Right-skewed</strong></p>
    <p><strong>2. Left-skewed</strong></p>
    <p><strong>3. Symmetric</strong> (frequently normally distributed)</p>
    <p>Depending on the shape associated with our dataset, certain measures of center or spread may be better for
      summarizing our dataset.</p>
    <p>When we have data that follows a <strong>normal</strong> distribution, we can completely understand our dataset
      using the <code>mean</code> and <code>standard deviation</code>.</p>
    <p>However, if our dataset is <strong>skewed</strong>, the <code>5 number summary</code> (and measures of center
      associated with it) might be better to summarize our dataset. </p>
    <hr>
    <h2>Outliers</h2>
    <p>Outliers have a larger influence on measures like the mean than on measures like the median. we should work
      with
      outliers on a situation by situation basis. Common techniques include:</p>
    <p><strong>1.</strong> At least note they exist and the impact on summary statistics.</p>
    <p><strong>2.</strong> If typo - remove or fix</p>
    <p><strong>3.</strong> Understand why they exist, and the impact on questions we are trying to answer about our
      data.</p>
    <p><strong>4.</strong> Reporting the 5 number summary values is often a better indication than measures like the
      mean and standard deviation when we have outliers. </p>
    <p><strong>5.</strong> Be careful in reporting. Know how to ask the right questions.</p>

    <h2>Box Plots</h2>

    <p>Identifying outliers and the shape associated with the distribution of our data are easier
      when using a visual as opposed to using summary statistics.
      <img src="https://www.simplypsychology.org/boxplot.jpg">
    </p>

    <h3>More On Center And Spread</h3>
    <p>When analyzing skewed data, it is common to report numeric summaries like the median and 5 number summary, as the
      mean and standard deviation may be misleading. </p>
    <p>However, with symmetric data, the mean and standard deviation are commonly used, as we can understand what
      proportion of points might fall 1, 2, or 3 standard deviations away based on the empirical rule associated with
      normal distributions.</p>

    <h3>Standard Deviation and Skewed Distributions</h3>
    <p>Standard Deviations can be calculated for any data set, whether it is normally distributed or skewed. So with the
      data below be careful what assumptions you are making about the underlying data.</p>
    <p>Also the standard deviation basically provides which of two sets of data are more spread out.</p>

    <h2>Descriptive vs. Inferential Statistics</h2>

    <h3>Descriptive Statistics</h3>
    <p><code>Descriptive statistics</code> <strong>is about describing our collected data</strong> using measures of
      center, measures of spread, shape of our distribution, and outliers. We can also use plots of our data to gain a
      better understanding.</p>

    <h3>Inferential Statistics</h3>
    <p><code>Inferential Statistics</code> <strong>is about using our collected data to draw conclusions to a larger
        population</strong>. Performing inferential statistics well requires that we take a sample that accurately
      represents our population of interest. </p>
    <p>A common way to collect data is via a survey. However, surveys may be extremely biased depending on the types of
      questions that are asked, and the way the questions are asked. </p>
    <li><strong>Population</strong> - our entire group of interest.</li>
    <li><strong>Parameter</strong> - numeric summary about a population</li>
    <li><strong>Sample</strong> - subset of the population</li>
    <li><strong>Statistic</strong> - numeric summary about a sample</li>

    <hr>

    ## SQL Aggregation

    ## NULLS

    NULLs are a datatype that specifies where no data exists in SQL.<p> Notice that <strong>NULL</strong>s are different
      than a zero - they are cells where data does not exist. </p>
    <p>When identifying <strong>NULL</strong>s in a <strong>WHERE</strong> clause, we write <strong>IS NULL</strong> or
      <strong>IS NOT NULL</strong>. We don't use <code>=</code>, because <strong>NULL</strong> isn't considered a value
      in
      SQL. Rather, it is a property of the data.</p>
    <h4>NULLs - Expert Tip</h4>
    <p>There are two common ways in which you are likely to encounter <strong>NULL</strong>s:</p>
    <ul>
      <li>
        <p><strong>NULL</strong>s frequently occur when performing a <strong>LEFT</strong> or <strong>RIGHT
            JOIN</strong>.
        </p>
      </li>
      <li>
        <p><strong>NULL</strong>s can also occur from simply missing data in our database.</p>
      </li>
    </ul>
    <h2>COUNT</h2>
    <p>Here is an example of finding all the rows in <strong>example</strong> table.</p>
    <pre><code>SELECT COUNT (*) FROM example;</code></pre>
    <p> we could have just as easily chosen a column to drop into the aggregation function:</p>
    <pre><code>SELECT COUNT (example.id)
FROM example;
</code></pre>
    <p>These two statements are equivalent, but this isn't always the case.</p>
    <p>Notice that <strong>COUNT</strong> does not consider rows that have <strong>NULL</strong> values. Therefore, this
      can be useful for quickly identifying which rows have missing data.</p>


    <p>Functionally, <strong>MIN</strong> and <strong>MAX</strong> are similar to <strong>COUNT</strong> in that they
      can
      be used on non-numerical columns. Depending on the column type, <strong>MIN</strong> will return the lowest
      number,
      earliest date, or non-numerical value as early in the alphabet as possible. As you might suspect,
      <strong>MAX</strong> does the opposite—it returns the highest number, the latest date, or the non-numerical value
      closest alphabetically to “Z.”</p>

    <p>Similar to other software <strong>AVG</strong> returns the mean of the data - that is the sum of all of the
      values
      in the column divided by the number of values in a column. This aggregate function again ignores the
      <strong>NULL</strong> values in both the numerator and the denominator.</p>

    <h2>GROUP BY / ORDER BY</h2>

    <ul>
      <li>
        <p><strong>GROUP BY</strong> can be used to aggregate data within subsets of the data. For example, grouping for
          different accounts, different regions, or different sales representatives.</p>
      </li>
      <li>
        <p>Any column in the <strong>SELECT</strong> statement that is not within an aggregator <strong>must be in the
            GROUP BY</strong> clause.</p>
      </li>
      <li>
        <p>The <strong>GROUP BY</strong> always goes between <strong>WHERE</strong> and <strong>ORDER BY</strong>.</p>
      </li>
    </ul>
    <h4>GROUP BY - Expert Tip</h4>
    <p>It is worth noting that SQL evaluates the aggregations before the <strong>LIMIT</strong> clause. If you don’t
      group
      by any columns, you’ll get a 1-row result—no problem there. If you group by a column with enough unique values
      that
      it exceeds the <strong>LIMIT</strong> number, the aggregates will be calculated, and then some rows will simply be
      omitted from the results.</p>

    <ul>
      <li>You can <strong>GROUP BY</strong> multiple columns at once.<br><br></li>
      <li>The order of columns listed in the <strong>ORDER BY</strong> clause does make a difference. You are ordering
        the
        columns from left to right.</li>
    </ul>
    <ul>
      <li>
        <p>The order of column names in your <strong>GROUP BY</strong> clause doesn’t matter—the results will be the
          same
          regardless. If we run the same query and reverse the order in the <strong>GROUP BY</strong> clause, you can
          see
          we get the same results.<br><br></p>
      </li>
      <li>
        <p>As with <strong>ORDER BY</strong>, you can substitute numbers for column names in the <strong>GROUP
            BY</strong>
          clause. It’s generally recommended to do this only when you’re grouping many columns, or if something else is
          causing the text in the <B>GROUP BY</B> clause to be excessively long.<br><br></p>
      </li>
    </ul>

    <h2>DISTINCT</h2>

    <p><strong>DISTINCT</strong> is always used in <strong>SELECT</strong> statements, and it provides the unique
      rows for all columns written in the <strong>SELECT</strong> statement. Therefore, you only use
      <strong>DISTINCT</strong> once in any particular <strong>SELECT</strong> statement.
    </p>
    <p>You could write:</p>
    <pre><code>SELECT DISTINCT column1, column2, column3
FROM table1;
</code></pre>
    <p>which would return the unique (or <strong>DISTINCT</strong>) rows across all three columns.</p>
    <p>You would <strong>not</strong> write:</p>
    <pre><code>SELECT DISTINCT column1, DISTINCT column2, DISTINCT column3
FROM table1;
</code></pre>
    <p> You can think of <strong>DISTINCT</strong> the same way you might think of the statement "unique". </p>
    <h4>DISTINCT - Expert Tip</h4>
    <p>It’s worth noting that using <strong>DISTINCT</strong>, particularly in aggregations, can slow your queries down
      quite a bit. </p>

    <h2>HAVING</h2>
    <p><strong>HAVING</strong> is the “clean” way to filter a query that has been aggregated, but this is also commonly
      done
      using a <a target="_blank" href="https://community.modeanalytics.com/sql/tutorial/sql-subqueries/">subquery</a>.
      Essentially, any time you want to perform a <strong>WHERE</strong> on an element of your query that was created by
      an
      aggregate, you need to use <strong>HAVING</strong> instead.</p>

    ``` SQL
    # Example
    SELECT COUNT(CustomerID), Country
    FROM Customers
    GROUP BY Country
    HAVING COUNT(CustomerID) > 5;
    ```
    <h2>DATE_TRUNC </h2>

    <p><strong>DATE_TRUNC</strong> allows you to truncate your date to a particular part of your date-time column.
      Common
      trunctions are <code>day</code>, <code>month</code>, and <code>year</code>. <a target="_blank"
        href="https://blog.modeanalytics.com/date-trunc-sql-timestamp-function-count-on/">Here</a> is a great blog post
      by
      Mode Analytics on the power of this function. </p>
    <p><strong>DATE_PART</strong> can be useful for pulling a specific portion of a date, but notice pulling
      <code>month</code> or day of the week (<code>dow</code>) means that you are no longer keeping the years in order.
      Rather you are grouping for certain components regardless of which year they belonged in.</p>
    <p>For additional functions you can use with dates, check out the documentation <a target="_blank"
        href="https://www.postgresql.org/docs/9.1/static/functions-datetime.html">here</a>, but the
      <strong>DATE_TRUNC</strong> and <strong>DATE_PART</strong> functions definitely give you a great start!</p>

    <h2>CASE</h2>
    <ul>
      <li>The <b>CASE</b> statement always goes in the SELECT clause.<br><br></li>
      <li><b>CASE</b> must include the following components: <b>WHEN</b>, <b>THEN</b>, and <b>END</b>. <b>ELSE</b> is an
        optional component to catch cases that didn’t meet any of the other previous CASE conditions.<br><br></li>
      <li>You can make any conditional statement using any conditional operator (like <a target="_blank"
          href="https://mode.com/resources/sql-tutorial/sql-where">WHERE</a>) between <b>WHEN and THEN</b>. This
        includes
        stringing together multiple conditional statements using AND and OR.<br><br></li>
      <li>You can include multiple WHEN statements, as well as an ELSE statement again, to deal with any unaddressed
        conditions.</li>
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

    <hr>

    <h2>Subquery Formatting</h2>
    <p>When writing <strong>Subqueries</strong>, it is easy for your query to look incredibly complex. In order to
      assist
      your reader, which is often just yourself at a future date, formatting SQL will help with understanding your code.
    </p>

    <h3>Badly/Well Formatted Queries</h3>
    <p>Though these poorly formatted examples will execute the same way as the well formatted examples, they just aren't
      very friendly for understanding what is happening!</p>
    <p>Here is the first, where it is impossible to decipher what is going on:</p>
    <pre><code>SELECT * FROM (SELECT DATE_TRUNC('day',occurred_at) AS day, channel, COUNT(*) as events FROM web_events GROUP BY 1,2 ORDER BY 3 DESC) sub;
</code></pre>
    <p>This second version, which includes some helpful line breaks, is easier to read than that previous version, but
      it
      is
      still not as easy to read as the queries in the <strong>Well Formatted Query</strong> section.</p>
    <pre><code>SELECT *
FROM (
SELECT DATE_TRUNC('day',occurred_at) AS day,
channel, COUNT(*) as events
FROM web_events 
GROUP BY 1,2
ORDER BY 3 DESC) sub;
</code></pre>
    <h3>Subqueries Part II</h3>

    <p>The <strong>WITH</strong> statement is often called a <strong>Common Table Expression</strong> or
      <strong>CTE</strong>. Though these expressions serve the exact same purpose as subqueries, they are more common in
      practice, as they tend to be cleaner for a future reader to follow the logic. </p>

    **Example**

    <pre><code>WITH table1 AS (
          SELECT *
          FROM web_events),

     table2 AS (
          SELECT *
          FROM accounts)


SELECT *
FROM table1
JOIN table2
ON table1.account_id = table2.id;
</code></pre>

    <hr>


    ## Data Cleaning
    <table>
      <thead>
        <tr>
          <th><strong>Statement</strong></th>
          <th><strong>How to Use It</strong></th>
          <th><strong>Other Details</strong></th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>LEFT</td>
          <td>LEFT(phone_number, 3)</td>
          <td>pulls a specified number of characters for each row in a specified column starting at the beginning (or
            from
            the left)</td>
        </tr>
        <tr>
          <td>RIGHT</td>
          <td>RIGHT(phone_number, 8)</td>
          <td>pulls a specified number of characters for each row in a specified column starting at the end (or from the
            right)</td>
        </tr>
        <tr>
          <td>LENGTH</td>
          <td>LENGTH(phone_number)</td>
          <td>provides the number of characters for each row of a specified column.</td>
        </tr>
        <tr>
          <td>STRPOS</td>
          <td>STRPOS(city_state, ',')</td>
          <td> takes a character and a column, and provides the index where that character is for each row. The index of
            the
            first position is 1 in SQL.</td>
        </tr>
        <tr>
          <td>LOWER</td>
          <td>LOWER(X)</td>
          <td>to make all of the characters lower. </td>
        </tr>
        <tr>
          <td>UPPER</td>
          <td>UPPER(X)</td>
          <td>to make all of the characters upper. </td>
        </tr>
        <tr>
          <td>CONCAT</td>
          <td>CONCAT(first_name, ' ', last_name)</td>
          <td><strong>CONCAT(first_name, ' ', last_name)</strong> or with piping as <strong>first_name || ' ' ||
              last_name</strong>.</td>
        </tr>
        <tr>
          <td>CAST</td>
          <td><strong>CAST(date_column AS DATE)</strong>.</td>
          <td><strong>CAST</strong> is actually useful to change lots of column types.</td>
        </tr>
        <tr>
          <td>COALESCE</td>
          <td><strong>COALESCE(COLUMN,X)</strong></td>
          <td>work with NULL values. </td>
        </tr>
      </tbody>
    </table>
    <hr>

    <h2> Data Visualization</h2>
    <p>For quantitative data, if we are just looking at one column worth of data, we have four common visuals:</p>
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

    <h3>Scatter plots</h3>
    <p>Scatter plots are a common visual for comparing two quantitative variables. A common summary statistic that
      relates
      to a scatter plot is the <strong>correlation coefficient</strong> commonly denoted by <strong>r</strong>.</p>
    <p>Though there are a <a target="_blank"
        href="http://www.statisticssolutions.com/correlation-pearson-kendall-spearman/">few different ways</a> to
      measure
      correlation between two variables, the most common way is with <a target="_blank"
        href="https://en.wikipedia.org/wiki/Pearson_correlation_coefficient">Pearson's correlation coefficient</a>.
      Pearson's correlation coefficient provides the:</p>
    <ol>
      <li>Strength</li>
      <li>Direction</li>
    </ol>
    <p>of a <strong>linear relationship</strong>. <a target="_blank"
        href="https://en.wikipedia.org/wiki/Spearman%27s_rank_correlation_coefficient">Spearman's Correlation
        Coefficient</a> does not measure linear relationships specifically, and it might be more appropriate for certain
      cases of associating two variables.</p>

    <img src="https://i.ibb.co/Kb92ZGb/image.png" alt="image" border="0">

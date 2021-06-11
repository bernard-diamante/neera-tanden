<h1>The Attitudes of Twitter Users towards the Nomination of Neera Tanden as Member of President-Elect Joe Biden’s Cabinet: A Thematic and Sentiment Analysis</h1>
<i>Text Analysis Project by Andrew Altuna, Bernard Diamante, Paolo Fuentes, and Jan Laguer</i><br>
<i>*Refer to the <a href="https://github.com/bernard-diamante/neera-tanden/blob/main/slides_deck.pdf">slides deck<a> for complete details and visualizations</i>
<hr>
<h2>Background of the Study</h2>
<ul>
  <li>On November 30, President-Elect Joe Biden announced his nomination of Neera Tanden as the Director of the Office of Management and Budget.</li>
  <li>According to Keith (2020), Tanden is getting the most pushback from U.S. politicians of all Biden’s announced picks for Cabinet positions.</li>
  <li>Pengelly (2020) of The Guardian reports that since her nomination, Tanden has deleted over 1,000 tweets that are targeted towards Republicans.</li>
  <li>Tanden’s confirmation will depend on whether or not Republicans keep control of the Senate after Georgia’s Senate run-off elections in January (CBS News, 2020).</li>
</ul>

<h2>Research Questions</h2>
<ol>
  <li>What are the <b>most frequently used words</b> by the Twitter users on the nomination of Neera Tanden as a Cabinet appointee of President-Elect Joe Biden?</li>
  <li>What are the <b>popular topics being discussed</b> by Twitter users?</li>
  <li>What is the prominent <b>polarity of sentiments</b> of Twitter users towards Neera Tanden?</li>
</ol>
<hr>
<h2>Methodology</h2>
<h3>Data Gathering</h3>
<p>Our data is gathered solely from Twitter using the RTweet package under the R programming language. The corpus consists of worldwide Tweets from November 27 to December 5, 2020 with the following search words:
  <ul>
    <li>Biden Neera Tanden (17,135)</li>
    <li>Neera Tanden Biden cabinet (4,234)</li>
    <li>Neera Tanden Biden appointee (2,892)</li>
    <li>Neera Tanden transition (883)</li>
    <li>Neera Tanden management (11,564)</li>
    <li>Neera Tanden budget (5,601)</li>
    <li>Neera Tanden plan (199)</li>
    <li>#Neera (62)</li>
    <li>#Tanden (220)</li>
    <li>#NeeraTanden (3,950)</li>
  </ul>
</p>
<h3>Parameters</h3>
<ul>
  <li>The chosen search words for our text mining aim to provide opinions of both sides of the spectrum: the supporters, and opposition of Neera Tanden as a newly-appointed member of Biden’s cabinet.</li>
  <li>We have encountered a hashtag: #NeeraTandenIsEvil; however, we decided against using this for our data mining as it was plagued with disinformation and may skew our results.</li>
  <ul>
    <li>We may use a hashtag that supports Neera Tanden as a way to balance out the results, but no such hashtag exists.</li>
    <li>Given this, we decided to use search words that are purely objective and do not necessarily have a biased political leaning such as the hashtag in question.</li>
  </ul>
  <li>Instead of using the search word “Neera Tanden”, we decided to make our search more specific to Neera Tanden as an appointed member of President Biden’s cabinet in order to filter out Tweets that have nothing to do with her position.</li>
  <ul>
    <li>On the other hand, we decided to use #NeeraTanden as it is trending and used often to voice out opinions regarding her position.</li>
  </ul>
</ul>
<h3>Data Cleaning</h3>
<ul>
  <li>After compiling all of the data gathered from text mining, we set <b>status_id as the primary key</b> and removed all duplicates based on this.</li>
  <li>Due to President Biden’s announcement regarding Neera Tanden’s appointment being on November 30, we filtered out mined Tweets that were created beforehand.</li>
  <li>For use of the necessary data analysis methods, <b>a list of stopwords will be utilized<b> in order to filter out “meaningless” words that have low TF-IDF scores.</li>
</ul>
<h3>Data Analysis</h3>
    <ul>
      <li>Frequency Analysis</li>
        <ul>
          <li>Count the most frequently used individual words and bigrams (collocation).</li>
          <li>In order to better understand the most salient words and bigrams, they will be subjected to data visualization in the form of a bar graph and a word cloud.</li>
        </ul>
      <li>Topic Modelling</li>
        <ul>
          <li>Subject dataset to Latent Dirichlet allocation (LDA) in order to determine the words that are grouped which connote a common topic.</li>
          <li>Determine most optimal value of K.</li>
          <li>Graph β (“beta”) through data visualization in order to determine the most common words found within a single topic.</li>
        </ul>
      <li>Sentiment Analysis</li>
        <ul>
          <li>Determine the feelings that Twitter users express in the mined tweets (positive and negative reactions).</li>
          <li>In order to achieve this, a list of words associated with strongly positive or negative sentiments will be created. </li>
          <li>Each positive and negative word in the dataset will then be counted and analyzed. </li>
          <li>The results will be graphed through data visualization in order to determine the differences of the positive and negative reactions in the dataset.</li>
        </ul>
    </ul>
<hr>
<h2>Overview</h2>
<p><b>Data Corpus</b><br> 
Consists of tweets obtained using keywords related to Neera Tanden and her appointment to office by President-elect Joe Biden.</p>
<p><b>Timespan (November 30 to December 8, 2020)</b><br> 
Nine days after Tanden’s announcement as the appointed director of the Office of Management and Budget (OMB).</p>
<p><b>Corpus Size</b><br> 
From a total of 48,788 Tweets in the original corpus reduced to 45,763 after cleaning duplicates.</p>

<h2>Ethics</h2>
<p><b>Anonymity</b><br>
Data mining using the Twitter API retrieves a lot of personal information such as usernames. To ensure anonymity, we reduce each data point to only the necessary columns we require for analyzing the tweets. This includes reducing data to tokens and pooling them into a bag-of-words.</p>
<p><b>Privacy</b><br>
Twitter users have an option to keep their Tweets private--available to only those who follow them. The researchers have only mined 'unprotected tweets' in order to keep the privacy of these users.
</p>

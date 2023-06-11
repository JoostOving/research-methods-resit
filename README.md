# Examining the Impact of Max Verstappen's First World Championship on Dutch Twitter
## General Information
This project analysis the frequency of 'formule 1' and 'f1' in the month where Max Verstappen became formula 1 world champion for the first time, the focus is Dutch tweets. 
The analysis uses a dataset from the Rijksuniversiteit Groningen, which contains all Dutch tweets.

## Research question and hypotheses
The research question for this study is: Did Max Verstappen's first world championship in formula 1 change the frequency of 'formule 1' on Dutch Twitter?

Hypothesis: 
- the frequency of 'formule 1' will be high around the time Max Verstappen became world champion, reflecting the reach of his influence in the Netherlands.

Variables:
- Independant: The date Max Verstappen became world champion for the first time in formula 1.
- Dependant: frequency of "formule 1" and "f1" on Twitter.

## Methods
The study uses the Dutch Tweet Corpus provided by the Rijksuniversiteit Groningen. For this research, we only used the month December of the year 2021, since Max Verstappen became world champion for the first time in this month. We analyzed the tweets by grouping them per day in the whole month. 

To collect the data: 
- Fill in your computer terminal: ssh sstudentnumber@karora.let.rug.nl
- Login with your credentials
- Run this codein the terminal of the twitter tool:
```
for day in {01..31}; do     file="/net/corpora/twitter2/Tweets/2021/12/202112${day}*.out.gz";     eval "count=\$(zless $file | /net/corpora/twitter2/tools/tweet2tab -i text | grep -iw 'formule 1' | wc -w)";     echo "Day $day: $count words"; done
```
and
```
for day in {01..31}; do     file="/net/corpora/twitter2/Tweets/2021/12/202112${day}*.out.gz";     eval "count=\$(zless $file | /net/corpora/twitter2/tools/tweet2tab -i text | grep -iw 'f1' | wc -w)";     echo "Day $day: $count words"; done
```

It will take some time to run these commands but after approximately 20-30 minutes depending on your laptop or pc all data should be gathered.

# References
-Rajput, N. K., Grover, B. A., & Rathi, V. K. (2020). Word frequency and sentiment analysis of twitter messages during coronavirus pandemic. arXiv preprint arXiv:2004.03925.
-Lee, R., & Sumiya, K. (2010, November). Measuring geographical regularities of crowd behaviors for Twitter-based geo-social event detection. In Proceedings of the 2nd ACM SIGSPATIAL international workshop on location based social networks (pp. 1-10).

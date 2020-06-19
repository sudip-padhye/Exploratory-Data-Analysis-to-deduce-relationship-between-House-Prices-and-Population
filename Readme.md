#Introduction
A researcher for a thinktank wants to learn about how house prices in the U.S. have changed over
the last few decades, and whether changes in prices are related to population in some way.She has
taken an introductory statistics course using R, but that was a long time ago, so she is outsourcing
the exploratory data analysis to YOU.

## Questions-
The researcher's major research question is: How have house prices in U.S. states changed
over the last few decades, and are changes in prices are related to population in some
way? This question may be difficult to answer, at least straight away. So she has brainstormed a
series of questions he would like you to address, which can be divided into groups:

1. House prices over time: How have house prices in the U.S changed since 1975, after
adjusting for in ation (i.e. relative to the CPI?) How have changes in prices varied by state?
Which states have seen the biggest increases in real house prices, and which have seen the
biggest decreases? Have changes in prices within each state mostly followed the same basic
pattern, and are there outliers to that pattern? Do the typical patterns vary between the
four regions (Northeast, Midwest, South, and West)?

2. Population density and changes in house prices: Does present-day population density
explain changes in house prices by state since 1975? Are there outliers to the relationship,
and if so, is there a principled reason to drop them? What does the relationship look like
after dropping or downweighting outliers? Does the relationship vary by region? If so, how?

3. Changes in population and changes in house prices: Is there a relationship between
changes in population and changes in house prices? To answer this, look at changes in each
state over three time periods: 1990 to 2000, 2000 to 2010, and 2010 to the present. Analyze
the three time periods separately. Has the relationship changed over the three time periods?
Are there variations by region?

4. Conclusion: What does all of this tell you about the relationship between house prices and
population? Is there a plausible cause-and-eect story you can tell that's consistent with the
data and with common sense?

## Data
1. Freddie Mac House Price Index (http://www.freddiemac.com/research/indices/
house-price-index.html): This tracks the average house price in each state (plus Wash-
ington, D.C. and a national average) since 1975. For each state, the index value is xed at
100 in December 2000. Figures are seasonally-adjusted but not adjusted for in
ation. The
data is in the spreadsheet State and US SA.xls.
2. state abbrevs.txt (on Canvas): This contains the names, the two-letter code, and the
Census region (Northeast, Midwest, South, or Midwest) for each state in the U.S.
3. Consumer Price Index, on Canvas in cpi.csv. This tracks how prices in general have
changed in the U.S. The data in the spreadsheet is the \All Urban Consumers (Current
Series)," seasonally adjusted, from www.bls.gov/cpi/data.htm.
4. Census Data: You'll need to get population data for each state in 2018, 2010, 2000, and
1990 from the Census and American Community Survey. We recommend you do this us-
ing the tidycensus R package. See https://walkerke.github.io/tidycensus/articles/
basic-usage.html for a description of how to use the package.

To use the package, you'll need a Census Data API key. To sign up for one, enter your email
at https://api.census.gov/data/key_signup.html and they'll send you a key (you'll have
to wait a few minutes for it to activate.) The main population variable is P001001 in the
2010 and 2000 Censuses, and P0010001 in the 1990 Census. If you can't get the data this
way, you can always get it directly from data.census.gov.

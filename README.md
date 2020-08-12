# Partisan Trends in Congressional Behavior
## *Increased party line voting under the Trump Administration*
### By Liz Timmons

I used a dataset from [fivethirtyeight](https://fivethirtyeight.com/)'s github repository, that included data on how often members of Congress vote in line with or against President Trump. I chose it because I wanted some insights on what Congress is like under the Trump Administration. The data was already cleaned and in usable form for the most part, but I had to standardize some string's values. For instance under the  `party` column, some values were D and R while others were Democrat and Republican. To do this, I first imported the CSV to [OpenRefine](https://openrefine.org/). I clicked `facet`> `text facet`> `cluster` in order to standardize the text strings' values to D, R or I across the CSV. I then exported the CSV to [Google Sheets](https://www.google.com/sheets/about/), where I formatted the `agree_pct` and `predicted_agree` columns' values to percents by going `format`> `number`> `percent`. 

Once the data was in workable form in Google Sheets, I put a filter view on my spreadsheet. There, I was able to sort the data from my columns from `A to Z` and `Z to A`. I sorted the `agree_pct` column, `predicted_agree` column and `net_trump_vote` column. I also filtered the `congress` column to show either only data from the 115 Congress or 116 Congress, the `chamber` column to show only data for Senate or House members, and the `party` column to show results for only one party. In doing so, I found some interesting data:

**Predicted Agree Percent versus Actual Agree Percent with Trump: Congresswoman Ocasio-Cortez**
1. **Congresswoman Ocasio-Cortez**, New York, Democrat, House -- `3.85% predicted_agree` versus `13.58% agree_pct`

 *I found this discrepancy interesting because I expected Congresswoman Ocasio-Cortez to have one of the lowest agree percents with Trump. I bet there are some confounders for this.*

**Highest Agree Percent with Trump in Congress**
1. **Congressman Marino**, Pennsylvania, Republican, House -- `100%`
2. **Congressman Zinke**, Montanta, Republican, House -- `100%`
3. **Congressman Chaffetz**, Utah, Republican, House --`100%`

**Lowest Agree Percent with Trump in the Senate**
1. **Senator Booker**, New Jersey, Democrat, Senate -- `10.34%`
2. **Senator Harris**, California, Democrat, Senate -- `11.11%`
3. **Senator Wyden**, Oregon, Democrat, Senate -- `12.82%`

**Highest Agree Percent with Trump in the Senate**
1. **Senator Loeffler**, Georgia, Republican, Senate -- `100%`
2. **Senator Braun**, Indiana, Republican, Senate -- `94.74%`
3. **Senator Crapo**, Idaho, Republican, Senate --`94.4%`

**Lowest Agree Percent with Trump of Senate Republicans**
1. **Senator Collins**, Maine, Republican, Senate -- `46.15%`
   *Key Decision: Voted with Trump to appoint Brett Kavanaugh to Supreme Court, while voted against Trump to repeal the Affordable Care Act*
2. **Senator Murkowski**, Alaska, Republican, Senate -- `58.33%`
3. **Senator Paul**, Kentucky, Republican, Senate -- `62.5%`

  *I especially found this interesting because Sen. Collins and Sen. Murkowski have been known as key bipartisan figures and "moderates" in the past in the Senate, but those notions have been questioned in the Age of Trump. Critics have suggested that both have moved away from their past bipartisanship especially with their  dual confirmation of Kavanaugh. And despite having the lowest agree percents of Republicans, their data supports this increased polarization.*

**Highest Agree Percent with Trump of Senate Democrats**
1. **Senator Manchin**, West Virginia, Democrat, Senate -- `33.33%`
2. **Senator Sinema**, Arizona, Democrat, Senate -- `26.32%`
3. **Senator Jones**, Alabama, Democrat, Senate -- `23.68%`

   *I found the gap between Sen. Collins, the Republican Senator with the lowest agree percent, and Sen. Manchin, the Democratic Senator with the highest agree percent, astonunding. Their is 13% margin in party line voting. In terms of the "across the aisle" analogy, that makes for a pretty wide aisle.*

I mostly focused on sorting with the Senate because of the **fillibuster**. The fillibuster makes party government operate differently in the Senate than the House. Fillibusters have become costless for the minority party, which is the Democratic Party under the Trump Administration. All they have to do is threaten to fillibuster and prevent the 60 votes for **cloture**, which is a 2/3 vote. Through this they can block most things in the Senate. Routine fillibuster and cloture has given rise to a lot of gridlock. Within the spatial model with a fillibuster, the most important position is either the 60th most liberal or 60th most conservative Senator, as they can invoke cloture. 

Thus according to sorting Senator's agree_pct with Trump from `Z to A`, the 60th most liberal Senator for a fillibuster would be **Democratic Senator Murphy** of Connecticut. And according to sorting conversely Senator's agree_pct from `A to Z`, the 60th most Conservative senator would be **Republican Senator Cotton** of Arkansas.
- Sen. Murphy agree percent with Trump -- `21.05%`
- Sen. Cotton agree percent with Trump -- `84.62%`

This discrepancy was very interesting to me, as this data depicts the intense partisanship we have in Congress through party voting behavior. It depicts how this intense partisanship has occurred under the Trump Administration and is demarked by the percentage members vote with or against Trump. It helped answer the question of if we can have intense partisanship and the filibuster.

**After I filtered and sorted my data in various different ways, I created various pivot tables with my data**. I did this by selecting `data`>`pivot table`. I focused on finding the average percent agreement with Trump across the different chambers, congresses and parties.
![Screenshot of my pivot table on the average agree_pct value](https://media.journalism.berkeley.edu/upload/2020/08/1597199493c212305.png)

I then found the sum of `net_trump_votes` by party in a pivot table.

Finally, I did a pivot table on the sum of `net_trump_votes` by state and the average of `agree_pct` by state. I used this specific data to input in my chart and chloropleth map in [Datawrapper](https://www.datawrapper.de/). 


<iframe title="Net Trump Votes by State" aria-label="Bar Chart" id="datawrapper-chart-z0wUQ" src="https://datawrapper.dwcdn.net/z0wUQ/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1240"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

<iframe title="Average Trump Agreement Percent by State" aria-label="map" id="datawrapper-chart-RzWjd" src="https://datawrapper.dwcdn.net/RzWjd/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="420"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

I found both of these to be interesting, as they depict the correlation between a state's average agree percent with Trump and their net votes with Trump, and if the state voted for Trump in 2016.

Beyond that, I selected different columns in my Google Sheets spreadsheet to create different charts. I sorted by chamber to show the average `agree_pct` of Congress in general, just the Senate and just the House. I also sorted to compare the average `agree_pct` of these with their average `predicted_agree` percent value.

### Average agreement percent with Trump

<iframe class= "d-block mx-auto" width="600" height="371" seamlessframeborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=1567075900&amp;format=interactive"></iframe>

<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSGtdkdFr_0-EKDv1aVJXCuSY7f75-ielNeIv505Fm0W4JVumuNN3aV1QRzkW_38HuQT0X111I74XR7/pubchart?oid=562984229&amp;format=interactive"></iframe>

<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSfsbtfuVgUMf5Gf4QjhWe6Y8r97_rfvxZHTwDGjYfbfaY8kKuyetG2RSDcUsYM9JzVkrRmTV4wxDQv/pubchart?oid=595790237&amp;format=interactive"></iframe>

### Average predicted versus actual agree percents with Trump

<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=124063791&amp;format=interactive"></iframe>

<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSGtdkdFr_0-EKDv1aVJXCuSY7f75-ielNeIv505Fm0W4JVumuNN3aV1QRzkW_38HuQT0X111I74XR7/pubchart?oid=639918220&amp;format=interactive"></iframe>

<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSfsbtfuVgUMf5Gf4QjhWe6Y8r97_rfvxZHTwDGjYfbfaY8kKuyetG2RSDcUsYM9JzVkrRmTV4wxDQv/pubchart?oid=1304994142&amp;format=interactive"></iframe>


### Average net votes with Trump in Congress 
 
<iframe class= "d-block mx-auto" width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=507834999&amp;format=interactive"></iframe>



### Graph analysis

The data shows how whether a member will vote in-line with Trump's position or not can be predicted be a member's political party affiliation. There is a positive correlation between being a Republican member of Congress and voting with Trump. On the other hand there is a postive correlation between being a Democratic member of Congress and voting against Trump's position. It suggests that party line voting is happening in both chambers of Congress, and that subsequently both chambers are polarized under the Trump Administration. 

The data also shows how congressional behavior is dictated by organization, as Congress has become increasingly polarized. This polarization has result in a party government organizational structure where members of each party engage in party line voting.  

Another interesting insight is how the indepdent political members of the House are more conservatively aligned, versus the more liberal aligned independent Senators. It shows how independent politicians are not cohesively aligned on the political spectrum, unlike the Democratic and Republican Parties. Both are clearly aligned on opposite spectrums of the political spectrum, as evident by their differences in agreement with Trump votes.

The data also suggests polarization and majority party line voting by depicting the absence of bipartisanship. It depicts how Republican and Democratic members have become polarizaed by revealing the large discrepancies between each parties' agreement and voting behavior patterns. It suggests the decline of moderates, as even the most "moderate" Republicans, Sen. Collins, has a agreement percentage of `46.15%` and voted against her state with her party and Trump in the confirmation of Brett Kavanaugh. 

Finally it suggests that Trump's views have become synonymous with that of the entire Republican parties', depicted in their overwhelming agreement and voting and patterns.

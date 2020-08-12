# Partisan Trends in Congressional Behavior
## Increased party line voting under the Trump Administration
### By Liz Timmons

I used a dataset from [fivethirtyeight](https://fivethirtyeight.com/)'s github repository, that includes data on how often each member of Congress votes in line with or against President Trump. I chose it because I wanted some insights of what Congress is like under the Trump Administration. The data was already cleaned and in usable form for the most part, but I had to standardize some string's values. For instance under the "party" column, some values were D and R while others were Democrat and Republican. To do this, I first imported the CSV to [OpenRefine](https://openrefine.org/). I clicked `facet`> `text facet`> `cluster` in order to standardize the text strings' values across the CSV. I then exported the CSV to [Google Sheets](https://www.google.com/sheets/about/), where I formatted the agree_pct and predicted_agree columns' values to percents by going `format`> `number`> `percent`. 

Once my data was in workable form in Google Sheets, I created put a filter view on my spreadsheet. There, I was able to sort the data from my columns from `A to Z` and `Z to A`. I sorted the agree_pct column, predicted_agree column and net_trump_vote column. I also filtered my congress column to show either only data from the 115 Congress or 116 Congress, my chamber column to show only data for Senate or House members and my party column to show results for only one party. In doing so, I found some interesting data:

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

  *I especially found this interesting, because Sen. Collins and Sen. Murkowski have been known as key bipartisan figures and "moderates" in the past in the Senate, but those notions have been questioned in the Age of Trump. Critics have suggested that both have moved away from their past bipartisanship especially with their  dual confirmation of Kavanaugh, and despite having the lowest agree percents of Republicans, their data supports this increased polarization.*

**Highest Agree Percent with Trump of Senate Democrats**
1. **Senator Manchin**, West Virginia, Democrat, Senate -- `33.33%`
2. **Senator Sinema**, Arizona, Democrat, Senate -- `26.32%`
3. **Senator Jones**, Alabama, Democrat, Senate -- `23.68%`

   *I found the gap between Sen. Collins, the Republican Senator with the lowest agree percent, and Sen. Manchin, the Democratic Senator with the highest agree percent, astonunding. Their is 13% margin in party line voting.*

I mostly focused on sorting with the Senate because of the **fillibuster**. The fillibuster makes party government operate differently in the Senate than the House. Fillibusters have become costless for the minority party, which is the Democratic Party under the Trump Administration. All they have to do is threaten to fillibuster and prevent the 60 votes for **cloture**, which is a 2/3 vote. Through this they can block most things in the Senate. Routine fillibuster and cloture has given rise to a lot of gridlock. Within the spatial model with a fillibuster, the most important position is either the 60th most liberal or 60th most conservative Senator, as they can invoke cloture. 

Thus according to sorting Senator's agree_pct with Trump from `Z to A`, the 60th most liberal Senator for a fillibuster would be **Democratic Senator Murphy** of Connecticut. And according to sorting conversely Senator's agree_pct from `A to Z`, the 60th most Conservative senator would be **Republican Senator Cotton** of Arkansas.
-Sen. Murphy agree percent with Trump -- `21.05%`
-Sen. Cotton agree percent with Trump -- `84.62%`

This discrepancy was very interesting to me, as this data depicts the intense partisanship we have in Congress through party voting behavior. It depicts how this intense partisanship has occurred under the Trump Administration and is demarked by the percentage members vote with or against Trump. It helped answer the question of if we can have intense partisanship and the filibuster.

**After I filtered and sorted my data in various different ways, I created various pivot tables with my data**. I did this by selecting `data`>`pivot table`. I focused on finding the average percent agreement with Trump across the different chambers, congresses and parties.
![Screenshot of my pivot table on the average agree_pct value](https://media.journalism.berkeley.edu/upload/2020/08/1597199493c212305.png)

I then found the sum of `net_trump_votes` by party.
![Screenshot of my pivot table on the sum of net_trump_votes](https://media.journalism.berkeley.edu/upload/2020/08/159719956646ae615.png)

Finally, I did a pivot table on the sum of `net_trump_votes` by state and the average of `agree_pct` by state. I used this specific data to input in my chart and chloropleth map in [Datawrapper](https://www.datawrapper.de/). 


graph analysis:
A tendency to vote with Trump or against can be predicted by party lines. There is a positive correlation between being a Republican member of Congress and voting with Trump. On the other hand there is a postive correlation between being a Democratic member of Congress and voting against Trump's position.

This shows how polarization has increased in Congress, by how voting mostly occurs along party lines.

does data reveal the end of moderates? shows increasing party line voting

party government


Here is some text. And I want to create a [link](http://wikipedia.url).

1. Here is a list
2. Another item
3. Third item

* Here is a bulleted list
* Another item
* Third item

![picture of cat](http://placekitten.com/400/300)

Here is some text.

More text.

Girls who `code`.

<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=1289788854&amp;format=interactive"></iframe>

The formula I used was:


```
=VLOOKUP("Something", A2:157, 1, false)
```

### Average agreement percent with Trump

1. Congress
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=1567075900&amp;format=interactive"></iframe>

2. Senate
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSGtdkdFr_0-EKDv1aVJXCuSY7f75-ielNeIv505Fm0W4JVumuNN3aV1QRzkW_38HuQT0X111I74XR7/pubchart?oid=562984229&amp;format=interactive"></iframe>

3. House
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSfsbtfuVgUMf5Gf4QjhWe6Y8r97_rfvxZHTwDGjYfbfaY8kKuyetG2RSDcUsYM9JzVkrRmTV4wxDQv/pubchart?oid=595790237&amp;format=interactive"></iframe>

### Average predicted versus actual agree percents with Trump

1. Congress
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=124063791&amp;format=interactive"></iframe>

2. Senate
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSGtdkdFr_0-EKDv1aVJXCuSY7f75-ielNeIv505Fm0W4JVumuNN3aV1QRzkW_38HuQT0X111I74XR7/pubchart?oid=639918220&amp;format=interactive"></iframe>

3. House of Representatives
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vSfsbtfuVgUMf5Gf4QjhWe6Y8r97_rfvxZHTwDGjYfbfaY8kKuyetG2RSDcUsYM9JzVkrRmTV4wxDQv/pubchart?oid=1304994142&amp;format=interactive"></iframe>

### Average agree percent with Trump by state
<iframe title="Average Trump Agreement Percent by State" aria-label="map" id="datawrapper-chart-RzWjd" src="https://datawrapper.dwcdn.net/RzWjd/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="420"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


### Average net votes with Trump in Congress (shows polarization)
 
<iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vTHajvZIPulaVg4CnUPxIKTRs7rUhfJ6vDNX5t-6NS9gokL3OknVIAQ1DD0kv7_Tjp3mX_M3Qh7FzlT/pubchart?oid=507834999&amp;format=interactive"></iframe>

### Net votes with Trump by state
Color coated by states who voted for Trump in 2016
<iframe title="Net Trump Votes by State" aria-label="Bar Chart" id="datawrapper-chart-z0wUQ" src="https://datawrapper.dwcdn.net/z0wUQ/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="1240"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

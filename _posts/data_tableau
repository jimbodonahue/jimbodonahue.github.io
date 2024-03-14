---
title: "Data Exploration with Tableau"
# excerpt_separator: "<!--more-->"
categories:
  - Blog
  - tableau
tags:
  - tableau
  - data science
  - exploration
---

# Exploring data with Tableau
========================

For a recent job application, I was asked to present a story from the [ACLED](jimbodonahue.github.io) dataset, using only North American data from the last few years. As the project was in Tableau, I decided to use that for my exploration. I present it here, either for insight into my process or inspiration for others.

The first thing I did was to go the the [codebook](https://acleddata.com/download/2827/). Turns out, the data are all events, with information on actors, location, and details, including a verbal description. I then loaded my data subset into Tableau for more exploration.

The first thing I tried was a heat map of events. This failed on two accounts. First, Canada is too far north for the general Tableau projection. Secondly, the vast majority of events occurred near the coasts, with hot spots in Illinois (Chicago), Ontario (Toronto), and other major population areas. People live in cities, and events happen where people are.

I then created a time series bar graph, which evolved into the first panel of my [completed dashboard](https://public.tableau.com/app/profile/james.d6132/viz/ACLEDDashboard/PossibleChangesinConservativeExtremismintheUS?publish=yes). I present it here in log scale for readability, but it was suggested that I use a [button](https://kb.tableau.com/articles/HowTo/how-to-create-buttons-to-swap-sheets) to switch between scales. A weekly period gave a good bandwidth. Daily depended too highly on the weekday (weekend), and monthly or quarterly lost the feel for the data. I then looked for key dates and event types.

This I achieved through filtering. I first decided to focus on the United States, as this had the most data. I then used the various event type and actor type variables, looking for a trend. However, this was less successful than hoped. Most of the peaks corresponded with the death of George Floyd, and since my subset of the data began shortly before the Covid-19 lockdown, I could say little about the differences between the Trump and Biden years. The only narrative that I found was an increase in non-protest violence (small groups harassing or attacking an individual, usually). However, ACLED never recorded more than five such events in a week, so I consider this to be rather weak evidence.

I then turned to some basic data transformations. Tableau does not allow for much more than basic calculations, so there would be no threshold VAR or such statistical shenanigans. However, the problem above regarding population density could easily be solved. I downloaded census data on population and 2020 presidential election data from the Federal Election Commission.  With these data in a simple spreadsheet, I joined these with the ACLED data using state names, a join that Tableau makes wonderfully simple. I could then observe events per capita and by political leaning at a state level.

This led to my most information-dense graph, the second in the dashboard. States are sorted by their number of events, as are the sizes of the circles for faster recognition. The colors represent partisan positions, following the standard red for Republican, blue for Democrat convention. Finally, the vertical alignment of the events corresponds to the events per capita. We quickly see that tiny, left-leaning Vermont loves to protest. However, there is no major takeaway outside of the fact that conservative states have fewer events.

Here, it is important to remember the nature of the data. This represents only the number or events, regardless of size or connection to others. While the state-level analysis brings nothing new, it rules out possibilities such as certain states being particularly active. For example, one might suspect protest-prone California to have significantly more events than average, as might Wyoming, the reddest state. Both are fairly close to average. It is not included, but these results were robust to filtering.

Where I did find a result was in filtering to include only political and identity militias. The line graph, smoothed with a moving average filter for readability, shows that militia actions with political goals started growing during the George Floyd protests and never stopped. The bar graph on the right presents the top ten groups identified. While not shown, I found in my analysis that none of the top twenty were left-wing. Those active, however, tend to be white nationalist or antisemitic. Again, ACLED groups these events by the goal of the event, not the organization. This implies that these extreme-right armed groups are actively trying to influence the government in some way, averaging two events per day at the end of 2023.

This is by no means proof of an imminent threat, nor does it make a causal argument. Different data would be needed for such claims. But that was not the point of this exercise. I wanted to find a story in the data, and I found Tableau quite helpful in exploring.

### Limitations

There were a few things I would have liked to try that were not possible in Tableau. While I could use RegEx to filter the "notes" variable, this contained at least one paragraph describing the event. Tableau is not able to handle language processing at this time beyond what RegEx can achieve. I had a similar problem with the "Tags" variable, being unable to select multiple tags without rewriting my RegEx query. Had it been necessary, I could have created dummy variables, but that is a slow workaround.

Additionally, it would have been nice to apply some more advanced time series tools, such as creating a VAR model to simulate certain shocks or testing the significance of the George Floyd protests. Such statistical tools are readily available in Python or R, and an econometrician would have to carry them out there and import results into Tableau. However, for quickly slicing the data by event and group, Tableau was a wonderful exploration tool.

    

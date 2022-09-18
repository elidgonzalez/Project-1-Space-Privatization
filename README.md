# Project-1-Space-Privatization

## Business Understanding
### Brief description
Space exploration has always been a personal interest of mine. Therefore using the data found in [here](https://www.kaggle.com/datasets/davidroberts13/one-small-step-for-data), I wish to explore the data and find out more about the privatization of space and how it compares to state run space launches. I will make a medium [Blog Post](https://medium.com/@arkhamknighthell/the-privatization-of-space-b9bfd76a18b2). To analyze this I propose three questions: 1) Are space launches increasing quantity and success rate? 2) Has the private sector become more dominant now? & 3) Are state-run or private-sector space launches more successful? 
### Are rockets launches increasing both quantity and success rate?
This is the first thing to analyze. The quantity and quality serve as an indicator of both the interest, and as a baseline to compare the two sectors.
### Has the private sector become more dominant now?
This question is where the focus begin on the quantity and whether or not the private sector has grown and by how much.
### Are state run or private sector space launches more successful?
Perhaps one of the things we care about is the efficiency. Therefore a comparison is needed to see if there are any differences in quality.
## Data Understanding
### Access and Explore
While exploring Kaggle for longer than I care to admit I found the data [here](https://www.kaggle.com/datasets/davidroberts13/one-small-step-for-data). Since I've always had an interest and the dataset had a 10.0 usability rating I immediately decided to use it. 
After finding the the data online I decided to look through the documentation I saw the following columns, Company Name, Location, Detail, Status of Rocket, Rocket, Status Mission, Country of Launch, Companys Country of Origin, Private or State Run, Date, & Time. I ultimately decided to initially look at the data from the Rocket (cost of rocket), Status Mission, Private or State Run, Year. Having chosen the columns I downloaded the data and start up Jupyter Notebook. 
### Python Libaries
With the Jupyter Notebook I decided to use the following python libraries: 1) numpy for working with arrays, 2) pandas for reading data and organizing them with dataframses, & matplotlib for visulaization of data. With these I felt ready to begin answering my questions. 
## Prepare Data
### Wrangle & Clean
To see if any rows or columns needed to be dropped, I checked for any nulls in the colums and found 78% missing values on the rocket column. As this was the only column with missing values I decided to ignore this column. Then I decided to look at the data by decade instead of year so I needed to create that column using Year column to assign it a decade. After creating a decade I removed all data from the 2020s decade becuase it's not complete. I also noticed that the data from the 50s was limited to they year 1957 onwards, but I decided to keep it because this was the starting point of the space launches. Ultimately this didn't require cleaning as the data seemed mostly clean for the columns I did use. There was only the need to add a single column from the rest of the columns.
## Are space launches increasing quantity and success rate?
### Analyse
This first question is important to guage both interest and "how good we've gotten" a lack of launches could suggest overall waning interest. Likewise if accuracy goes down. There might be something more to look into such as whether or not the engineers who knew what to do retired. 
### Visualise
![](https://github.com/elidgonzalez/Project-1-Space-Privatization/blob/main/Space_Success_by_Decade.png)
### Explain the visualisation
For volume, we see the launches go from 51 in the 50s, possibly because launches started in 1957, to over 1012 in the 70s. Then launches suggested waning interest and funding with about a 40% drop, dropping to about 600 each decade in the 80s and 90s. The 2000s sees another drop to 475 before picking back up to 676 in the last decade of the 2010s. This rise suggests that we were very interested in space exploration until the 70s, then interest dropped until the 2000s, and then again picked back up in the 2010s. While the levels have not reached the 70s, it may be possible that interest will again get high in this decade. Success rates range from 31.4% in the 50s, most likely because it was in its infancy, to 93.68% in the 80s. We see the most significant increases in the 60s and 70s. After that, the success rate seems to level off with percentages in the low 90 range.
## Has the private sector become more dominant now?
### Analyse
Since our ultimate goal is to look at the overall privitzation of space, the first thing is to look a the number of launches for both sectors.
### Visualise
![](https://github.com/elidgonzalez/Project-1-Space-Privatization/blob/main/Launches_Private_vs_State.png)
### Explain the visualisation
At first glance, it's evident that the number of launches was first dominated by state-run entities from the 50s to the 80s. Then starting from the 90s, the share of launches became more even, with the private sector running most of the launches from then onwards.

From the graph, we can see that the negative trend in space did continue from the 70s to the 2000s in state-run space launches, at least from state-run launches. The private sector seems to have kept the launch numbers from completely dipping too far. As of now, space exploration has become more of a private-sector endeavor.
## Are state-run or private-sector space launches more successful?
### Analyse
The success rates are also important as these can be costly endeavors. We want these to succeed as much as possible.
### Visualise
![](https://github.com/elidgonzalez/Project-1-Space-Privatization/blob/main/Successes_Private_vs_state.png)
### Explain the visualisation
During the 50s, neither the state-run nor private sector had great success. The lone private sector launch failed. For this reason, I will leave it our comparison.

For the launches, we see that from the 60s to the 80s, there is a slight edge for state-run launches. During this time, the max difference in percentages was about 3.83% in the '70s.

After that, from the 90s onwards, it has gone to the private sector, having higher success rates. While the difference may seem low (0.2%), it was the first time the private sector could outperform state-run launches. Since then, the trend has seen more significant increases, with a 4.62% difference in the 2010s.
## Evaluation
### Findings
The privitization of space definitely seems to be a growing trend and also seems to be having more success these days. However, this was a only surface level analysis. To check out more information about launches is needed. As an example the rocket column had much missing data about the cost (not even considering costs adjusted for inflation). It would also be useful to see if there's a way to classify launches based on difficulty and see if the numbers may show a different insight. There are many ways to improve this including seeing if it's possible to add predictors. Perhaps at a later time with more data & experience I will explore these.

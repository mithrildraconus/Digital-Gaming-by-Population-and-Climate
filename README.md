# Digital-Gaming-by-Population-and-Climate
As our world has evolved into a society that is strongly technological and digitized, our culture of entertainment is strongly influenced and molded by those changes – an influence that I believe has exploded exponentially with the current pandemic and the guidelines for social distancing that have been enacted in order to minimize and curb its effects.  This is of particular interest to me as I hope to one day use my data science knowledge to merge both AI and VR, which is a concept that would have strong applications in the realm of video gaming.

Through the combination of the United States Census data for the 2018: ACS 5-Year Estimates Data Profiles – details age, gender, income, and like demographic information pulled from https://data.census.gov/cedsci/map?layer=VT_2018_050_00_PY_D1&cid=DP05_0001E&tid=ACSDP5Y2018.DP05&hidePreview=false&vintage=2018&g=0100000US.050000, the annual precipitation and average temperature data from 2000-2020 for all regions in the United States as pulled from the National Centers for Environmental Information data for the National Oceanic and Atmospheric Administration (https://www.ncdc.noaa.gov/cag/), and gameplay and ownership data for the top 100 games for the Steam digital gaming platform as pulled from the SteamSpy API (https://steamspy.com/api.php), this project's goal was to compare the details of the locations found in the data with the Steam gaming data to determine trends about the location and demographics of gamers across the continental United States as well as trends for those games purchased in those same demographics and locations.

By taking the information provided by each source this project attempted to create a map for the general layout of how digital games from the Steam platform are distributed across the continental United States both in measurements of their quantity and disbursement of such details as their genres, degree of online and/or multiplayer play, etc., as well as plot charts that compare the relationships between the demographics provided by both the census data and the climate data to attempt to determine if there are trends in the mentioned distributions to such details as age, gender, income, climate, etc., that determine the types, quantity, and styles of games that are purchased and played across the country.

## Project Process
In order to  merge all three data sets required first taking the census data and connected the various states found in the Locations column to their associated regions according to the information from the website https://www.ncdc.noaa.gov/:
• Northeast: Connecticut, Delaware, Maine, Maryland, Massachusetts, New Hampshire, New Jersey, New York, Pennsylvania, Rhode Island, Vermont
• Upper Midwest: Iowa, Michigan, Minnesota, Wisconsin
• Ohio Valley: Illinois, Indiana, Kentucky, Missouri, Ohio, Tennessee, West Virginia
• Southeast: Alabama, Florida, Georgia, North Carolina, South Carolina, Virginia
• Northern Rockies: Montana, Nebraska, North Dakota, South Dakota, Wyoming
• South: Arkansas, Kansas, Louisiana, Mississippi, Oklahoma, Texas
• Southwest: Arizona, Colorado, New Mexico, Utah
• Northwest: Idaho, Oregon, Washington
• West: California, Nevada

After merging the climate and census data sets using an outer join, the SteamSpy game data was randomly distributed into each of the nine regions and merged to the other data through another outer join; the resulting data set had 108 columns and over 6.5 million instances.  In reviewing the columns for the census data, most were found to not to match the desired information for the analysis and were therefore removed, resulting in a final cleaned data set with 28 columns and 6830663 instances.

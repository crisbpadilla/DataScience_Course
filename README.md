# Capstone project_ Coursera by IBM

## Space X data analysis using IPA and BeautifullSoup with Python

### Abstract
  Space X is a private company that had lead in the last period of time the sub-orbital and orbital private space travel, Falcon 9, being the last and more succesfull project at the moment, as they have reduced the cost of putting its rockets in orbit into space in comparisson with other companies, representing about a 38% of the cost incurred by the competition. This mainly is due the recovery of the first stage in the launching process (Falcon 9 have two stages that are separeted on the trayectory of the rocket), usin technology that will allow withstand reentry burns and the safety landing of the first stage.
  The idea of this project is to used two different tools to extract information about the space rocket launched by Space X, using an API and webscraping with BeautifulSoup, we will obtain the information of the Falcon 9 rocket launched, founding this data in the Space X webpage and in wikipedia, using the tool mention before respectively.
Once the <b> html data is converted into a DataFrame </b> it will be possible to wrangling the data to set it up for further analysis.
  Different kind of information can be obtain and create visualization to forseen insights trought the graphs and also determined if spacial X will reuse the first stage using the gathered data.

### Webscraping using API
 In the first part of this project the data was obtain using an API, for this matter jupyter notebook was used, getting great part of the code from the lab material given by IBM developers. This material was used to obtain the historical data, but at the same time dive deeper in the coding related with this task. 
 The code that includes analysis and personal insigths it is in this link <a href= 'SpaceX_webscraping.ipynb'> Web Scraping using IPA <a/>. 
### webscraping using beutifulSoup 
  The second tool used was parsering the data using <b>BeautifulSoup</b> object, for this matter, the course material was completed and the code given by the platform (IBM by coursera) <a href='jupyter-labs-webscraping.ipynb'> Lab webscraping using BeautifulSoup by IBM developers</a>.
  So, as the intention of understanding the methods and coding used, also was created another Jupiter notebook file with all the analysis of the different coding used in this project and developing an alternative way to parsing data with beautifulSoup object <a href='SpaceX_Soup.ipynb'> Code Training to obtain data using beautifulSoup(complete)<a/>. Obtaining the historical data of the rocket launched in between 2010 and 2019 from the webpage <link>https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches_(2010%E2%80%932019</link>

## Data Wrangling
 The data base has different fields of importance as:
 Date: date of launching.
 Orbit: Spacial orbit that the rocket aim to reach.
 Payload: fuel load used in stage one measure in kg.
 Outcome: concatenation of boolean variable of success or failure plus the landing dock or surface.
 
 For this part, the outcome category was considered to identify the success of failure of the first stage landing of the falcon 9 rockets. This values were storage in a new column named 'Class' that contains a binary response where '0' are the fail landings and '1' the ones that succeded. The code can be find in <a href='https://github.com/crisbpadilla/DataScience_Course/blob/main/labs-jupyter-spacex-Data%20wrangling%20(1).ipynb' > Data wrangling landing Outcomes </a> (not yet updated)
## Data analysis and visualizations

  Folium is another package in python that allows to work with maps and coordinates using markers, points, polygons and other figures to visualized data on a map. This library was used to identify the launch sites in the map and show a count of the success and fails launch of the falcon 9 <a href='https://github.com/crisbpadilla/DataScience_Course/blob/main/lab_jupyter_launch_site_location.jupyterlite.ipynb'> IBM lab to Map analysis </a> . In this laboratory, the main visualizations obtain were as follow:
  * Create a circular radius around the unique values of the launch sites, obtained using the grouoby function. Using the first coordinate as the value associated to long and lat.
  * create markers with red color for the launch that have failed and green for those that have succeded.
  * create a cluster marker object to visuaized the the markers group by faill and success launches.
  * determined the distance between a specific launch site coordenates to four different reference points (coast line, highway,railway and closer city).
### creating a dashboard

  Creating a dashboard using Dash package, a dahsboard was created with dropdown object using the attribute option to select the launching sites from the DataFrame. two graph were created, a pai chart with the sites and their success rate and a scatter plot with the correlation between the payload and the outcome of the launch, where also it is possible to select the payload weight using a slider. This dashboard was used to answered the next questions:
<b>Which site has the largest successful launches?</b>.
KSC LC-39A has 41.7% of success, the highest among the Launching sites.
<b>Which site has the highest launch success rate?</b>.
KSC LC-39A has the largest launch succes with a 76.9% of success.
<b>Which payload range(s) has the highest launch success rate?</b>.
 Considering all the sites, between 300 kg and 5400 kg are the highest success rate, specially for the buster version B5, that has 100% of success but taking in account that there is only one launch for this particular version, so it is not deterministic.
<b>Which payload range(s) has the lowest launch success rate?</b>
 Depending of the booster model, the failure rate and the range of success changed notoriously:
 *The model V.1.0 has the maximum failure rate, as 100% of the launches has a negative outcome.
 * Second worst failure rate is for the next model V.1.1, both of them between 0 kg and 5000 kg.
 * So considering this, the payload range with the maximum failure rate would be between [500,1900],[3700,4600] and over 5300 kg.
<b>Which F9 Booster version (v1.0, v1.1, FT, B4, B5, etc.) has the highest launch success rate?</b>
  b5 as it has just one sucesfull launch.

# Capstone project_ Coursera by IBM

## Space X data analysis using IPA and BeautifullSoup with Python

### Abstract
  Space X is a private company that had lead in the last period of time the sub-orbital and orbital private space travel, Falcon 9, being the last and more succesfull project at the moment, as they have reduced the cost of putting its rockets in orbit into space in comparisson with other companies, representing about a 38% of the cost incurred by the competition. This mainly is due the recovery of the first stage in the launching process (Falcon 9 have two stages that are separeted on the trayectory of the rocket), usin technology that will allow withstand reentry burns and the safety landing of the first stage.
  The idea of this project is to used two different tools to extract information about the space rocket launched by Space X, using an API and webscraping with BeautifulSoup, we will obtain the information of the Falcon 9 rocket launched, founding this data in the Space X webpage and in wikipedia, using the tool mention before respectively.
Once the <b> html data is converted into a DataFrame </b> it will be possible to wrangling the data to set it up for further analysis.
  Different kind of information can be obtain and create visualization to forseen insights trought the graphs and also determined if spacial X will reuse the first stage using the gathered data.

### Webscraping using API
 In the first part of this project the data was obtain using an API, for this matter jupyter notebook was used, getting great part of the code from the lab material given by IBM developers. This material was used to obtain the historical data, but at the same time dive deeper in the coding related with this task. 
 The code that includes analysis and personal insigths it is in this link <a href= 'SpaceX_webscraping.ipynb'> Web Scraping using IPA </a>. 
### webscraping using beutifulSoup 
  The second tool used was parsering the data using <b>BeautifulSoup</b> object, for this matter, the course material was completed and the code given by the platform (IBM by coursera) <a href='jupyter-labs-webscraping.ipynb'> Lab webscraping using BeautifulSoup by IBM developers</a>.
  So, as the intention of understanding the methods and coding used, also was created another Jupiter notebook file with all the analysis of the different coding used in this project and developing an alternative way to parsing data with beautifulSoup object <a href='SpaceX_Soup.ipynb'> Code Training to obtain data using beautifulSoup(complete)<a/>. Obtaining the historical data of the rocket launched in between 2010 and 2019 from the webpage <link>https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches_(2010%E2%80%932019</link>

## Data Wrangling
(not yet updated)
## Data analysis and visualizations

  Folium is another package in python that allows to work with maps and coordinates using markers, points, polygons and other figures to visualized data on a map. This library was used to identify the launch sites in the map and show a count of the success and fails launch of the falcon 9 <a href='https://github.com/crisbpadilla/DataScience_Course/blob/main/lab_jupyter_launch_site_location.jupyterlite.ipynb'> IBM lab to Map analysis </a> . In this laboratory, the main visualizations obtain were as follow:
  * Create a circular radius around the unique values of the launch sites, obtained using the grouoby function. Using the first coordinate as the value associated to long and lat.
  * create markers with red color for the launch that have failed and green for those that have succeded.
  * create a cluster marker object to visuaized the the markers group by faill and success launches.
  * determined the distance between a specific launch site coordenates to four different reference points (coast line, highway,railway and closer city).
  

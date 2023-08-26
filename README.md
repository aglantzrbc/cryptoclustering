# cryptoclustering

Glantz Adam Bootcamp RUT-VIRT-DATA-PT-04-2023-U-LOLC-MWTH - Module 19

# Crypto-Clustering Challenge

## TABLE OF CONTENTS

1. Project Description
2. Installation
3. Contributing
4. Acknowledgements
5. Licenses

### 1. PROJECT DESCRIPTION

In this [project](https://bootcampspot.instructure.com/courses/3337/assignments/54011?module_item_id=961925), the goal is to use [Python](https://www.python.org/) (particularly through the [sklearn](https://en.wikipedia.org/wiki/Scikit-learn) library) and [unsupervised machine learning](https://en.wikipedia.org/wiki/Unsupervised_learning) to predict if [cryptocurrencies](https://en.wikipedia.org/wiki/Cryptocurrency) are affected by 24-hour or 7-day price changes.

- **Prepare the Data and Find the Best Value for `k` Using the Original Data**

After investigating the data, sklearn's [StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html) was used in preprocessing to [normalize](https://en.wikipedia.org/wiki/Normalization_(statistics)) all dimensions of the data on a single scale. The best value for `k` (i.e., the nunber of [clusters](https://developers.google.com/machine-learning/clustering/overview#:~:text=In%20machine%20learning%20too%2C%20we,relies%20on%20unsupervised%20machine%20learning.)) was calculated by running [K-Means](https://serokell.io/blog/k-means-clustering-in-machine-learning) 11 times on the dataset and plotting the results, thereby using the [Elbow method](https://www.analyticsvidhya.com/blog/2021/01/in-depth-intuition-of-k-means-clustering-algorithm-in-machine-learning/) heuristic to determine when minimizing inertia (i.e., the [within-cluster sum of squares (WCSS))](https://support.minitab.com/en-us/minitab/21/help-and-how-to/statistical-modeling/multivariate/how-to/cluster-k-means/interpret-the-results/all-statistics-and-graphs/#:~:text=The%20within%2Dcluster%20sum%20of%20squares%20is%20a%20measure%20of,a%20large%20sum%20of%20squares.) is balanced by dimishing returns in adding more clusters.

**Question 1:** What is the best value for `k`?

**Answer:** It was demonstrated that the best value for `k` = _4_. After that point, the line becomes mostly horizontal, because more clusters only reduce the inertia by a small amount. See **Figure 1**.

![image](https://github.com/aglantzrbc/cryptoclustering/assets/127694342/2926e66c-4803-4097-a6f8-6a7e8c8557e5)

**Figure 1** | *Elbow curve for `k` (number of clusters) using the original normalized data*

K-Means was then used to train the data to produce four clusters of the relationship between 24-hour and 7-day cryprocurrency price changes. The value of clustering is that the machine can determine and display patterns it discovers by itself. See **Figure 2**.

![image](https://github.com/aglantzrbc/cryptoclustering/assets/127694342/75334f78-6eba-43ba-97d8-2e10dfe5b18c)

**Figure 2** | *Predicted clusters from the original normalized data of the relationship between 24-hour and 7-day cryptocurrency price changes.*

### 2. INSTALLATION

- The [GitHub](https://github.com/aglantzrbc/leaflet-challenge) repository (version 2.9.1) containing all project files is publicly accessible.
- **Constituent program files and their locations:**
  -  _HTML:_ **index.html** -- located at root level (run this file)
  -  _CSS:_ **style.css** -- located in the _css_ subdirectory one level below the root level
  -  _JAVASCRIPT_ (Mapbox API access token): **config.js** -- located at root level
  -  _JAVASCRIPT_ (main JavaScript file): **logic.js** -- located in the _Leaflet-Part-1_2_ subdirectory one level below the root level
- **If the relative placement of files, above, is altered, the code won't run.**
- The program relies upon regular updates from the two source URLs at periodic intervals. At times, imperfections or interruptions in the connection may cause a reduction in functionality, such as the inability to toggle layers. **When this happens, it is recommended that the user refresh their browser.** _Please note that alerts in the platform console may occur, but do not necessarily mean function is impaired._
  - Another way to deal with resource access issues is to spin up a local server using [cross-origin resource sharing (CORS)](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing), such as through the [Git](https://git-scm.com/) command "python -m http.server", and run the code through a local port, ideally via a private or incognito browser window or tab. 
- The program's Mapbox functionality is provided by an API access token individually supplied to the author. The terms of use may change over time or the token's utility may expire, causing the program to no longer function as intended. **If this happens, it is recommended that the user obtain their own access token from [Mapbox](https://www.mapbox.com/about/maps/) and update the _config.js_ file.** _Please see the bottom of this README document for access to terms of use for the Mapbox API and its major associated functionality source._
- The assignment details and starter code are proprietary and located on the [Rutgers University](https://www.rutgers.edu/) [(edX)](https://www.edx.org/) Bootcamp Spot [Module 15 Leaflet Challenge](https://courses.bootcampspot.com/courses/3337/assignments/54007?module_item_id=961640) webpage.
- The latest versions of the coding languages are [CSS3](https://en.wikipedia.org/wiki/CSS), [HTML5](https://en.wikipedia.org/wiki/HTML5), and [JavaScript ES13](https://en.wikipedia.org/wiki/JavaScript).
- This project was created on a [PC](https://en.wikipedia.org/wiki/Personal_computer) using [Google Chrome](https://www.google.com/chrome/) for [Windows](https://www.microsoft.com/en-us/windows) version 115.0.5790.102 and its associated [Google DevTools](https://developer.chrome.com/docs/devtools/) extension. **If the program doesn't function, it is recommended that the user attempt running it on this platform and browser.**
- Coding was guided by the [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself) ("don't repeat yourself") principle.

### 3. CONTRIBUTING

- [Glantz, Adam](https://www.linkedin.com/in/adam-glantz/): Annapolis, Maryland, USA, July 2023, email: adamglantz@yahoo.com

### 4. ACKNOWLEDGEMENTS

In addition to using the resources listed above, the author acquired query responses in OpenAI's [ChatGPT](https://chat.openai.com/) 3.5 and 4 platforms, and the [VSCode GitHub Copilot](https://github.com/features/copilot) app V1.

The author also consulted code and results from similar projects publicly accessible in [GitHub](https://github.com/) repositories and recoverable through [Google](https://www.google.com/) and comparable search engines:

- [Cooper, Tanisha](https://www.linkedin.com/in/tanisha-cooper-5b3743197/): Locust Grove, Georgia, USA, July 2022. [leaflet-challenge](https://github.com/TanishaCooper/leaflet-challenge)
- [Janer, Jordan](https://www.linkedin.com/in/jordan-janer/): Los Angeles, California, USA, February 2022. [leaflet-challenge](https://github.com/JordanJaner/leaflet-challenge)
- [Tallant, Jeremy](https://www.linkedin.com/in/jeremy-tallant-717075220/): San Antonio, Texas, USA, February 2023. [leaflet-challenge](https://github.com/JeremyTallant/leaflet-challenge)
- [Zhu, Jiuhe (Rosa)](https://www.linkedin.com/in/jiuhe-zhu/): Chicago, Illinois, USA, October 2020. [leaflet-challenge](https://github.com/Jiuhe2020/leaflet-challenge)

The full citations for the JSON data used in this project are as follows:

- [Ahlenius, Hugo](https://www.linkedin.com/in/hugoahlenius/), [Nordpil](https://nordpil.com/): Stockholm, Sweden, October 2014. [tectonicplates](https://github.com/fraxen/tectonicplates)
- [United States Geological Survey](https://www.usgs.gov/), Earthquake Hazards Program: Reston, Virgina, USA. [GeoJSON Summary Format](https://earthquake.usgs.gov/earthquakes/feed/v1.0/geojson.php)


### 5. LICENSES

- **Use of this program assumes the user is in compliance with the terms of service for the [Mapbox](https://www.mapbox.com/legal/tos) API and for the API Mapbox uses as a source, [OpenStreetMap](http://www.openstreetmap.org/copyright).**
- Otherwise this program is allowed for free use via the [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) license.

# The Persistence of Tuberculosis Storymap
Tuberculosis, or TB, is a disease that usually attacks the lungs, but they can also damage other parts of the body which can lead to death. In the past about a couple centuries, Tuberculosis killed more people than any other disease in the world. Today, Tuberculosis is now known as the leading killer of people who are HIV-positive and one of ten highest causes of death around the world. Yet, many people from wealthy households are unconcerned with the disease that has such a high mortality rate. How is it that a disease considered inconsequential to one country can be such a huge problem for another nation entirely? Why does Tuberculosis continue to persist when advancements in medicine have already created treatments for it? This project aims to explain and represent how Tuberculosis persists in the world despite the numerous technological and medical advancements already developed. This project was made using the Storymap javascript library and the maps were created in QGIS using data gathered from the World Health Organization.

The Storymap javascript library allows indivduals with little web programming experience to create story map applications over the internet. A storymap is organically integrated by several scenes. Each scene consists of a web map and a script. The project opens with the title of the Storymap showing the purpose of the project as well as a video showing a rendered example of how Tuberculosis infects the human body. In the top-left corner of the Storymap are two icons. The first icon is a link the leads to the github repository of the project while the second icon opens an info page explaining what the project is about and what the functions of the project are. The rest of the storymap is several maps showing a chloropeth-style dataset in each map talking about what each dataset means among the United States, Canada, Brazil, Peru, and Argentina.

- The first map compares modern TB rates between the countries with an associated legend
- The second map compares TB rates of the countries from the year 2000 and explains how TB rates have changed over time
- The third map shows the amount of funding each country spends on TB per million each year and how that has affected TB rates over the years
- The fourth map talks about the number of doctors in each country and how that has affected TB rates over the years
- The fifth and final map shows the percentage of GDP used for health expenditure to show how much each country cares about treating health
- The next scene of the storymap is teh conclusion which analyzes the overall data to explain TB's persistence, but also the best path that is needed to treat it
- The storymap ends with a credit scene thanking the viewer for taking their time to read the storymap

With these things in mind, this storymap is designed to attract the average U.S. citizen to get them thinking about preventable diseases that threaten developing countries. This project is made to have people thinking about how they can help developing nations and the best way to help them. This project is made by Darren Snguon, an undergaduate of the University of Washington Geography Department.

## The System Architecture
This project is being hosted by Github, a code hosting platform for version control and collaboration. It lets anyone work together on projects from anywhere. It also allows people to create and host both personal websites (one allowed per user) and websites related to specific GitHub projects.

As for the internal code of the project, it uses html, css, and javascript to form the interface of the website. It gets its css and javascript from the *storymap.js* javascript library. The *index.html* file links to the location of the *storymap.js* and *storymap.css* files of the most recent build, in this case being version 2.5. The storymap javascript library uses leaflet and bootstrap to provide the javascript and css of the project. Leaflet is an open-source JavaScript library for interactive web maps. It's lightweight, simple, and flexible, and is probably the most popular open-source mapping library at the moment. It is capable of converting data to map layers and mouse interactions working well with almost all devices. It can add tilemaps and basemaps to a website that visitors can interact with. Storymap uses leaflet for the interactive javascript which creates the maps and other graphics of the website. Bootstrap is a free front-end framework for easy web development. Bootstrap creates easy to understand website templates for people to use to make their websites with. Storymap uses bootstrap to form the easy to make scenes and info cards found within the project.

The tilemaps found in the project were created using QGIS, a GIS software capable of creating geospatial data. The data of the maps were made thanks to data found from the [World Health Organization](https://www.who.int/) website. After the geospatial data was created, it was converted into the tilemaps found within the project to represent the maps found in each scene. The video and image assets were found searching on YouTube and Google to fit a title and end scene for the storymap project.

## The Code
The code of the project starts off with linking to the storymap library:

    <!--add required stylesheets-->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css">
    <!--leaflet css-->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.4.0/leaflet.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.7.2/css/all.css">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.4.0/dist/leaflet.css"/>


    <!--add favicon for the web page-->
    <link rel="shortcut icon" href="../../img/favicon.ico" type="image/x-icon">

    <!--Fonts-->
    <link href="https://fonts.googleapis.com/css?family=Cairo" rel="stylesheet">


    <link rel="stylesheet" type="text/css" href="css/storymap.2.5.css">
    <!--add required libraries-->

    <script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet/1.4.0/leaflet.js"></script>
    <!--jquery-->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.0/umd/popper.min.js"></script>

    <!--boostrap-->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js"></script>
    <!--leaflet.ajax for asynchronously adding geojson data-->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/leaflet-ajax/2.1.0/leaflet.ajax.min.js"></script>

    <script src="https://unpkg.com/leaflet@1.4.0/dist/leaflet.js"></script>

    <!--story map plugin-->
    <script src="js/storymap.2.5.js"></script>

This code snippet is what allows the entire project to work seemlessly within itself. It creates the storymap library from the bootstrap and leaflet libraries which allow the storymap to be made. The leaflet libraries it uses help to create the interactive maps of the project while the bootstrap libraries help to create the template of the website. This Storymap libary already comes with supported responsive design which allows most devices to view the website of the project without issue.

## Data Sources and Web Elements
![WHO](assets/WHO.png)
The data used in this project was acquired from the World Health organization's own dashboard about Tuberculosis. The website shows how Tuberculosis affects each country and the funding each country puts in to combat the disease.

![GIS](assets/GIS.png)
This data was then converted into Geospatial data represented by chloropeth maps to show the disparity of values in each map. The basemap used for these maps is CartoDB's Positron basemap because it is a grayscale basemap capable of easily showing the color-coded data of chloropeth maps. Each country is color-coded on a graduating scale to show that the darker colors represent the higher values of the data the map represents.

The map elements found in the website only consist of a legend for each map and an info page button and a Github button. The legend is personalized for each map depending on the data scale and the buttons in the top-left corner are designed to allow the visitor access to the website's info and the github repository.

## Strengths and Weaknesses
Stengths | Weaknesses
-------- | ----------
Respresent Tuberculosis data in an easy to read and understand set of geospatial maps | Incapability of interacting with the maps other than the legend
Highly responsive design depending on the device used to view it | Somewhat difficult to read fonts and sizing
Maps easy to analyze to understand goal of project | Exact values of data placed in weird places

## Reflection
To conclude, this entire project was made to explain and represent how Tuberculosis persists in the world despite the numerous technological and medical advancements already developed. It aimed to explain the inequalities of Global health through the disease of Tuberculosis.

In 2002, it was reported that TB had been exposed to over one third of the Ethiopian population and one third of those cases resulted in fatality (The Global Fund). It is difficult to think that a disease many Americans think is now harmless to them can be such a prevalent killer in another country altogether. But to nations such as Ethiopia, Tb was and still is a dangerous threat to the health of their people. These numbers alone were contributed by the fact that many of these developing nations did not have the proper health systems in place to treat TB. “Social unrest, limited numbers of trained health workers, inadequate health facility networks and management problems all create obstacles to care” (World Health Organization). Simply put, in 2005, many African countries had no proper ways to fight against TB which lead to a public health emergency throughout the continent. The lack of resources in developing nations makes it difficult to treat people and since people are spending time being sick rather than healthy, they are not making money which also hurts the economy of their country resulting in a poorer nation. This cycle continues until someone intervenes by providing the nations with funding to combat their healthcare issues. Thus, The Global Fund was made to provide Structural Adjustment Programs for these countries to help them fight against any issues they suffer from that can be corrected to help them catch up to developed nations. With these new funds, developing nations began to build their own health systems to reduce cases of TB and other diseases. Power began to shift between the Global North and South.

In the year 2000, it was theorized that “The nature of relationships between North and South must change and is changing to account for the closing gap in capacity to carry out research of international standard. The development of a lexicon sophisticated enough to adequately address these changing relationships, however, lags behind and is not supported by the mindless recourse to the jargon of “partnership”” (Ogden and Porter). The developing nations of the south were no longer a group of countries that were incapable of solving its issues. Now they were trying to reach similar standards found in the North to reach a level of recognized equality between the global hemispheres. The developed countries of the North were now invested in Global problems as the world became more interconnected. The North recognized the importance of countries from the South and became more willing to help with their issues by providing funding because it is not that they are incapable of becoming developed because of their own faults but rather the circumstances that befell them. Health is becoming a serious issue to these people as more investment became drawn to the world stage. The South only suffered from poor health conditions because of the lack of help in their economies to jumpstart them and the North was too conceited to recognize this. Paul Farmer recognizes that health is a difficult thing to process for everyone equally because not all places are made equal (Paul Farmer). If the North wants to make a world where health is essential instead of a luxury, it must take into account how many of these countries do not have healthcare systems in the first place and will need help to create them. Thus, developed nations over the next decade sought to become more philanthropic and developing nations began to acquire the help that it needed to build its systems. The health of developing nations steadily improved as shown “financial development leads to reduction in under-five mortality rate as well as improved life expectancy” (Chireshe and Ocran). However, they are still nowhere close to the level of developed nations at all. Whereas developed nations have over 300 antibiotics to treat bacteria, developing nations will probably have around at most 20.

In 2017, Ethiopia still showed around 15% of the population suffering from cases of Tuberculosis. Advancements are being made that is helping to treat TB, but these advancements are very slow considering that the technologies already exist to treat it. So what exactly is making this slow development? Particularly, it is the fact that, while they are providing funding now, most of the health funding goes into researching diseases that affect developed nations over developing nations. Illnesses such as cancer receive much more funding than tuberculosis by the sheer fact that most of the economic decisions are made by mostly the developing nations. Developed nations think they know what is best for the world and try to control everything about it. However, the reality is developing nations are capable of solving their problems if they had the funding to do so. Developed nations do not need to tackle everything and try to solve it through their colonial mindset. Many countries are deeply involved with their problems and know how to solve them on their own such as in Nigeria, they suggest “the integration of Health Impact Assessment into public policy” (Chilaka and Ndioho) because the majority of the population agrees that is would benefit their health care. TB’s persistence could end if developing nations were recognized for their efforts and rewarded for it so that they could continue in their research that they know works best for them. In India, they suffer from a large TB problem as well and even though they don’t receive much funding they will make it work because they know “this risk could be mitigated using modern adherence support mechanisms” (Arinaminpathy). As a result, in the beginning, developed countries were ignorant to the plight of Tuberculosis in developing nations, but over time, they began to provide assistance to developing nations healthcare systems and now has reached a point where these developing nations can now lead their own healthcare with funding from the developed nations.

## References
Arinaminpathy, Nimalan, et al. "The Potential Deployment of a Pan-Tuberculosis Drug Regimen in India: A Modelling Analysis." PLoS ONE, vol. 15, no. 3 (2020): 1-14. EBSCOhost, doi:10.1371/journal.pone.0230808.

Chilaka, Marcus A. and Ibiangake Ndioho. "Health Impact Assessment in Nigeria: An Initiative Whose Time Has Come." Journal of Public Health in Africa, vol. 10, no. 2 (2020): 68*72. EBSCOhost, doi:10.4081/jphia.2019.1014.

Chireshe, Jaison and Matthew K Ocran. "Financial Development and Health Outcomes in Sub-Saharan African Countries Journal of Developing Areas." Journal of Developing Areas, vol. 54, no. 3 (2020): 145-159. EBSCOhost, doi:10.1353/jda.2020.0030.

Ogden, Jessica A. and John D. H. Porter. "The Politics of Partnership in Tropical Public Health: Researching Tuberculosis Control in India." Social Policy & Administration, vol. 34, no. 4 (2000): 391. EBSCOhost, doi:10.1111/1467-9515.00198.

Paul Farmer, et al. Reimagining Global Health : An Introduction. University of California Press, 2013. ProQuest Ebook Central.

The Global Fund. "Ehtiopia TB/HIV Funding Request." 2017. Document.

—. "Proposal Tuberculosis - R01." 2002. Document.

Tougher, Sarah, et al. "ACCESS TO DRUGS. Improving Access To Malaria Medicine Through Private-Sector Subsidies In Seven African Countries." Health Affairs, vol. 33, no. 9 (2014): 1576-1585. EBSCOhost, doi:10.1377/hlthaff.2014.0104.

World Health Organization. "Curing More Patients, Saving Lives." 2005. Web.

—. "The End TB Strategy." 2020. Web.

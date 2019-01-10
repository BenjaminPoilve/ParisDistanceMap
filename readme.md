# A subjective Map of Paris

##### A map showing how long it takes you to go somewhere.
|Host|link|
|---|---|
| Github | [:link:](https://github.com/BenjaminPoilve/ParisDistanceMap/blob/master/main.ipynb)   |
|  NBviewer |  [:link:](https://nbviewer.jupyter.org/github/BenjaminPoilve/ParisDistanceMap/blob/master/main.ipynb) |

The goal of this project was to create a map of Paris that would allow me to know how long it would take to go somewhere with just one glance. 

Here is the result:

![](./data/La Muette (METRO), Paris.png)


To compare with the one of my girlfriend:

![](./data/Marcadet - Poissonniers (METRO), Paris.png)


#### How to use

This is a python notebook, so you can easily launch it on your computer. 

You can define your station in the fifth code block. 

It does take a little while (around 30 minutes), for two reasons:

* I hit the RATP website and I did not want to hit them too hard. So no threading in the scrapping. 
* I didn't optimise the fonction calculating the distance per pixel. This is not good at all. Since walking speed is constant, Delaunay Triangulation should help me there (as my dad suggested it), but I did not have the time to think about it yet! 


#### How it works

It's pretty straightforward.

* I used wikipedia to scrape the station list and their geolocations
* I had to clean the file manually to fit the RATP nomination
* I mapped the location to pixels in a map I grabbed on OpenStreetMaps
* I scrape the time from the defined station to all the other stations (thanks to the RATP)
* I use it to build an image (supposing constant walk speed between the stations)
* I had a map overlay! 

You can find an article about this on [my blog](http://benjaminpoilve.com/projects/#)

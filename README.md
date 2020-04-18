
# Bing COVID-19 Widget 
As the coronavirus impacts the world, we recognize the need to share the latest information outside of Bing. This widget will allow any site to easily add an outbreak map, the latest case counts, and a chart displaying the spread over time. These elements are modular, giving sites the ability to customize the experience. Learn more on how to embed and customize the widget for your needs below.  

**By using the widget, you agree to be subject to the terms of use [listed here](../master/LICENSE)**

## How can I embed the widget on my site?
You will simply need to add two lines of HTML code, a ```<div>``` including various widget parameters, and a ```<script>```. At the bottom of this readme are code examples for the various supported configurations. Each configuration is a combination of three supported modules: an **Outbreak Map Module** showing the worldwide spread of the virus, a **Data Stats Module**, which displays the case count information for a given location, and a **Trends Chart Module** showing the spread of the virus in a location over time. Note that the **Trends Chart Module** has limited market support at this time. 

## How do I select a widget configuration?
You are able to select your widget configuration with the ```data-type``` parameter. We support the following values:

| Description   | ```data-type``` Parameter |
| --------- |:---------------------:|
| Default – includes all three modules: Outbreak Map module, Trends Chart module, and Data Stats module | covid19 |
| Map – includes only the Outbreak Map module | covid19_map |
| Trends – includes only the Trends Chart module | covid19_trends |
| Stats and Map – includes the Data Stats module and Outbreak Map module | covid19_stats_map |
| Stats and Trends – includes the Data Stats module and Trends Chart module | covid19_stats_trends |


In addition to these ```data-type``` options, you can also stack multiple widget on top of each other by including multiple ```<div>``` lines and only one ```<script>```. 

In the future we plan to support additional configuration options and will update the GitHub with any

## How do I select the market and language?
The ```data-market``` and ```data-language``` parameters control the market and language of the widget respectively. The market refer to the country/region the widget will optimize for. The language referes to the UI display language in which the widget will display the UI string resources. Typically you will have the  ```data-market``` and ```data-language``` set to the same parameter value, however, there are cases where they would differ. For example, you can have a user in United States who speaks Spanish. In this case you can set the ```data-market``` to en-US and the ```data-language``` to es-ES. We support the following values for  ```data-market``` and ```data-language```:

| Market   |  ```data-market``` Parameter |
| --------- |:---------------------:|
| Australia | en-AU                 |
| Canada | en-CA |
| Canada* | fr-CA |
| France* | fr-FR |
| Germany* | de-DE |
| India | en-IN |
| Italy* | it-IT |
| Japan* | ja-JP |
| South Korea* | ko-KR |
| Spain* | es-ES |
| UK | en-GB |
| US | en-US |

* Markets with an asterisk (*) do not support the ```data-type``` of ```covid19_stats_trends``` currently. 

  
| Language   |  ```data-language``` Parameter |
| --------- |:---------------------:|
| English in Australia | en-AU |
| English in Canada	| en-CA |
| English in India	| en-IN |
| English in | UK 	en-GB |
| English in | US	en-US | 
| French  | 	fr-FR |
| French in Canada  | 	fr-CA |
| German | 	de-DE |
| Italian | 	it-IT |
| Japanese | 	ja-JP |
| Korean | 	ko-KR |
| Spanish | 	es-ES |


## How do I specify a location for the widget to load?
The ```data-location-id``` parameter allows you to set location based on a set of available ```“/Country/Region"``` combinations. A list of the supported locations is available in the [AllLocations.txt file](../master/AllLocations.txt). If no ```data-location-id``` is set, the default is the global view. You can also select a global view for the data-location-id parameter with a vlaue of ```"/"```. 

In the future we also plan to support location selection by latitude and longitude values and will update this readme once it is available. 

## Widget examples

**By using the widget, you agree to be subject to the terms of use [listed here](../blob/master/LICENSE)**


### Widget Default
See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/78/)
```
<div class="bingwidget" data-type="covid19" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

Default widget example setting language and market to Japanese in Japan. See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/77/)
```
<div class="bingwidget" data-type="covid19" data-market="ja-jp" data-language="ja-jp"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

### Widget with only Map

See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/74/)

```
<div class="bingwidget" data-type="covid19_map" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

Map only widget example specifying location of Italy. See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/73/)
```
<div class="bingwidget" data-type="covid19_map" data-market="en-us" data-language="en-us" data-location-id="/Italy"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

### Widget with only Trends
See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/70/)
```
<div class="bingwidget" data-type="covid19_trends" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

### Widget with Stats and Map
See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/66/)
```
<div class="bingwidget" data-type="covid19_stats_map" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```
Stats and Map widget example specifying location of United States. See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/68/)
```
<div class="bingwidget" data-type="covid19_stats_map" data-market="en-us" data-language="en-us" data-location-id="/United States"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```


### Widget with Stats and Trends
See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/64/)
```
<div class="bingwidget" data-type="covid19_stats_trends" data-market="en-us" data-language="en-us"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```
Stats and Trends widget example specifying location of Texas. See it live [here](https://jsfiddle.net/covidwidget/xby7f2h6/63/)
```
<div class="bingwidget" data-type="covid19_stats_trends" data-market="en-us" data-language="en-us" data-location-id="/United States/Texas"></div>
  
<script src="//www.bing.com/widget/bootstrap.answer.js" async=""></script>
```

## How can I report issues I have found with the widget?
Please email bingcovidwidget@microsoft.com with any issue reports. 

## Known Issues:
* The “Powered by Bing” and “Explore more on Covid-19 tracker” are new additions to the wisget and the strings ares still being translated into the languages we support. 
* There is additional white colored padding around the widget that can be seen on sites with a colored backgound. 

## Where is the widget data from and how often does it update?
The widget refreshes approximately every ten minutes with data from an aggregate of [sources](https://help.bing.microsoft.com/#apex/18/en-us/10024) Bing is consuming. Data may not change with every refresh. 

## Can I download the source data?
Bing is making our COVID-19 available for educational and academic purposes. Get the data and learn more at the [Bing COVID-19 Data GitHub page](https://github.com/microsoft/Bing-COVID-19-Data). 

<a href="http://www.stator-afm.com/">![Stator](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/stator_icon.png?raw=true)</a>

## Stator AFM (Visual Studies)

<a href="http://www.stator-afm.com">**Stator AFM**</a> is easy to use portfolio management software for traders and investors. Stator is highly analytical and comes with a free visualisation add-on allowing users to go nuts creating interesting visualisations of their financial, trading and investing data.

> The visual studies in this repository are compatible with add-on version 3.3.16230+

## Before we go on, explain what Stator is again?

To put this in simple terms, Stator is portfolio management software. Ever seen the movie <a href="http://www.imdb.com/title/tt0094291/">'Wall Street'</a> or <a href="http://www.imdb.com/title/tt0993846/">'The Wolf of Wall Street'</a>? Well it's software that can be used by those individuals as well as any other, down-to-earth trader or investor. It's more than likely the people using Stator are more like you and I than Gordon Gekko!

Visit the website to learn more:
<a href="http://www.stator-afm.com">Stator AFM website</a>

And yeah, I am the human that wrote Stator so <i>send me some love if you don't mind</i>!

## Table of contents
 
* [Team Members](#team-members)
* [What is visual studies?](#what-visual)
* [Show me pictures](#show-pictures)
* [How does it work?](#how-work)
* [The data domains within Stator](#data-domains)
* [The underlying data](#data)
* [The development environment](#ide-environment)
* [I want to contribute](#contribute)
* [License](#license)
 
## <a name="team-members"></a>Team Members
* Anthony Nosek (<anthonynosek@gmail.com>)
* You?

## <a name="what-visual"></a>So this visual studies functionality, why did you create it?

I wanted to give users of Stator as much flexibility as possible in analysing their data. With the evolution of HTML5 and javascript visualisation libraries it was only natural that someone (aka me) try and merge everything into desktop software. The end result is a free add-on that leverages HTML5 technology directly in the desktop environment.

Stator exposes data at various '[domains](#data-domains)' within the software and users can write visualisations using any of the popular visualisation libraries available. At the current time visual studies supports the following libraries:

> <a href="http://chartjs.org/">![Chart](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_chartjs.png?raw=true)</a> 
> <a href="http://d3js.org/">![D3](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_d3js.jpg?raw=true)</a> 
> <a href="http://nickqizhu.github.io/dc.js/">![DC.js](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_dcjs.jpg?raw=true)</a> 
> <a href="http://dygraphs.com/">![Dygraph.js](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_dygraphsjs.jpg?raw=true)</a>
> <a href="http://echarts.baidu.com/">![ECharts](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_echarts.png?raw=true)</a>
> <a href="http://paperjs.org/">![Paper.js](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_paperjs.jpg?raw=true)</a> 
> <a href="http://processingjs.org/">![Processing.js](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_processingjs.jpg?raw=true)</a> 
> <a href="http://raphaeljs.com/">![Raphael.js](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/icon_raphaeljs.jpg?raw=true)</a> 

Those are the big boys of javascript visualisation libraries right there, from left to right they are:

* <a href="http://chartjs.org/">Chart</a>
* <a href="http://d3js.org/">D3 - Data Driven Documents (version 3 or 4+)</a>
* <a href="http://nickqizhu.github.io/dc.js/">DC - Uses D3 v3</a>
* <a href="http://dygraphs.com/">Dygraphs</a>
* <a href="http://echarts.baidu.com/">ECharts</a>
* <a href="http://paperjs.org/">Paper</a>
* <a href="http://processingjs.org/">Processing</a>
* <a href="http://raphaeljs.com/">Raphael</a>

Please note: <i>Visual studies functionality has been designed in such a way that supporting new libraries is a piece of cake. We've tried to make visual studies as future-proof as possible.</i>

## <a name="show-pictures"></a>Enough already, a picture is worth a thousand words

Here are a couple of pictures that should give you an idea what visual studies is all about. Normally, within Stator data is displayed in tabular form, for example we do this when displaying open or closed positions. This is a very traditional way of displaying information to a user and can often hide patterns within the data that we should look to explore and learn from.

![markets domain](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/visualstudies_chartdataexample.jpg?raw=true)

<i>Markets Charting data domain</i>

![position domain](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/visualstudies_closedpositiondataexample.jpg?raw=true)

<i>Open Positions data domain</i>

What can be seen in the two pictures above are **two alternatives to the same underlying data**. The data repository is shown on the left, it looks like a dark barrel. On the right are two images, the default Stator screen is shown above and an alternative visualisation of the same data shown underneath.

**And the picture below...** This is a visual study generated in Stator for closed positions. This is a cluster plot of close position profit/loss. It gives you an idea what is possible with visual studies, the code for this visualisation is provided in this repository.

![ide](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/131002_D3ClosedPositionClusterWithProfit.png?raw=true)

## <a name="how-work"></a>How does it work?

**Great question!**

## <a name="data-domains"></a>What are the data domains within Stator?

At the current time you can write visualisations for the following data domains (internal to Stator):

1. None - you obtain your own JSON
2. Markets - Charting
3. Markets - Watchlist
4. Home - Summary
5. Estate - Summary
6. Estate - Cash accounts
7. Estate - Cash transactions
8. Estate - Diary entries
9. Estate - Position statistics
10. Estate - Open positions
11. Estate - Income
12. Estate - Closed positions

## <a name="data"></a>What's the format of the underlying data?

**JSON** - (JavaScript Object Notation) is a lightweight data-interchange format.

JSON is easy for humans to read and write and easy for machines to parse and generate. The following code extract is an example of data in JSON format. I am sure you already know this...

```
{
	"widget": {
		"debug": "on",
		"window": {
			"title": "Sample Konfabulator Widget",
			"name": "main_window",
			"width": 500,
			"height": 500
		}
	}
}
```

For the various data domains Stator exposes the data in JSON format. Each visualisation study automatically allocates the data to a variable which you can use in your visualisation. And depending upon which visualisation library you choose will determine the code syntax that you'll write.

## <a name="ide-environment"></a>How do I write code, what is the development environment?

Creating the functionality to display visualisations within Stator wasn't enough. I needed to enable users to write and execute code (visualisation code) within Stator. I had know other choice than to write a custom development environment (<i>integrated development environment [IDE])</i> within Stator.

![ide](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/131002_DCStockMarketPriceDataInIDE.png?raw=true)

<i>Visual studies development environment</i>

## <a name="contribute"></a>I would like to contribute my time and expertise

**I'd like that!**

There are a couple of things you need to do before you can start contributing or writing your own visual studies. These requirements are listed below:

1. <a href="http://www.stator-afm.com">Download and install Stator</a>  
   Inside the Stator installation folder will be two empty folders called:   
   * "visual studies" 
   * "visual studies libraries"
   
	![install](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_installfolders.png?raw=true)

2. <a href="http://www.stator-afm.com/about-stator-visualisation-studies/">Download the visual studies add-on</a>   
   Downloading the visual studies add-on is simply downloading all the library files that Stator requires in order to load the visualisations. **After you install visual studies** the libraries folder should contain files such as:  

	![libraries](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_installfoldersvisuallibraries.png?raw=true)

3. Read through the visual studies installation guide
4. Open the visual studies IDE
5. **Start coding, experimenting and creating your own awesome visualisations!**

## <a name="license"></a>License information

These visual studies are intended to be used with Stator - Advanced Finance Management software. If you create anything new and exicting please let the community know. That's all, **play nice!**

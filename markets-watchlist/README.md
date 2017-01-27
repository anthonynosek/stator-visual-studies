## Data Domain: Markets-Watchlist
Stator AFM (Visual Studies)

### Domain explanation
Stator exposes meta data AND latest price data for each ticker in the watchlist.

### Where are canvases for this domain found within Stator?
1. **Watchlist Screen**  
   From the main Stator screen select "Markets" and "Watchlists".

### JSON data format
- Two tickers are shown in the example below:
 	General Electric (GE)
	Alcoa Inc (AA)
- Date is in yyyy-MM-dd HH:mm:ss format (HH = 24 hour notation).
- If no price is retrieved the dictionary value is NULL ("v": null)

```json
[
    {
        "k": {
            "Identifier": "GE",
            "Category": "",
            "Description": "",
            "WatchList": {
                "Name": "Dow Jones",
                "Description": ""
            },
            "BaseType": {
                "ClassificationCountry": "United States",
                "ClassificationType": "Exchange",
                "Description": "NYSE Stock Exchange (NYS)",
                "Identifier": "X_USA_NYSE"
            },
            "Template": {
                "Name": "Google Finance",
                "PluginID": "GOOGLE"
            }
        },
        "v": {
            "DateTime": "2013-06-26 14:00:00",
            "Open": 0,
            "High": 0,
            "Low": 0,
            "Close": 23.32,
            "Volume": 0,
            "OpenInterest": 0,
            "Change": 0.07,
            "Identifier": "NYSE:GE",
            "Misc": null,
            "ErrorMessage": null
        }
    },
    {
        "k": {
            "Identifier": "AA",
            "Category": "",
            "Description": "",
            "WatchList": {
                "Name": "Dow Jones",
                "Description": ""
            },
            "BaseType": {
                "ClassificationCountry": "United States",
                "ClassificationType": "Exchange",
                "Description": "NYSE Stock Exchange (NYS)",
                "Identifier": "X_USA_NYSE"
            },
            "Template": {
                "Name": "Google Finance",
                "PluginID": "GOOGLE"
            }
        },
        "v": {
            "DateTime": "2013-06-26 14:00:00",
            "Open": 0,
            "High": 0,
            "Low": 0,
            "Close": 7.87,
            "Volume": 0,
            "OpenInterest": 0,
            "Change": 0.12,
            "Identifier": "NYSE:AA",
            "Misc": null,
            "ErrorMessage": null
        }
    }
]
```

### Accessing the data from a visual study
Inserted code (HTML)
- This code is automatically inserted into the page HTML for single sketch studies only.
- Variable 'dataWatchlist' contains the JSON data for watchlist, item/ticker, template, price and volume.

```javascript
<script>
function getJsonData(url) {
       var data = null;
       $.ajax({
               'url': url,
               'async': false,
               'global': false,
               'dataType': "json",
               'success': function(json) {
                               data = json;
                           }
       });
       return data;
}
</script>

<script>
var dataWatchlist = getJsonData('##JSON_DATA_FILE##');
</script>
```

## Visual studies in this repository for this data-domain

* [Percentage change treemap (D#.js)](#d3-tree)
* [Percentage change pack layout grouped (D3.js)](#d3-pack)

## <a name="d3-tree"></a>Visual Study: Percentage Change Treemap (D3)

![stator_d3treemap](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-watchlist-percent_change_treemap-d3.png?raw=true)

(Above) Percentage change treemap layout. The size of each tile is related to turnover (latest price x volume), the colour- related to the magnitude of percentage change, i.e. bright green for large positive moves, bright red for large negative moves. Visualisation created using Data Driven Documents, D3.js and Stator.  
Author: Anthony Nosek

## <a name="d3-pack"></a>Visual Study: Percentage Change Pack Layout Grouped (D3)

![stator_d3pack](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-watchlist-percent_change_pack-layout-d3.png?raw=true)

(Above) Percentage change pack layout grouped by category using D3.js. Tickers are grouped by category (user defined), the size of each ticker circle is related to turnover (latest price x volume) and color related to the magnitude of percentage change. The visualisation shown above is the ASX50 index @ 27th January 2017-11:20AM.  
Author: Anthony Nosek

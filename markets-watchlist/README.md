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
<i>None at the time of writing.</i>

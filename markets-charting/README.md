## Data Domain: Markets-Charting
Stator AFM (Visual Studies)

### Domain explanation
Stator exposes price, time series data for this data domain. When a user selects one (or multiple) securities Stator will expose the underlying price data (open, high, low, close, volme) via a JSON file that is loaded into a variable.

### Where are canvases for this domain found within Stator?
1. **Charting Screen**
   From the main Stator screen select "Markets" and "Charting"

### JSON data format
- Each data point is represented by the following JSON.
- Date is in yyyy-MM-dd HH:mm:ss format (HH = 24 hour notation).

```json
[
    {
        "DateTime": "2013-01-02 13:00:00",
        "Open": 1.456585,
        "High": 1.482289,
        "Low": 1.430881,
        "Close": 1.473721,
        "Volume": 195979,
        "OpenInterest": 0,
        "Change": 0,
        "Identifier": null,
        "Misc": null,
        "ErrorMessage": null
    }
]
```

### Accessing the data from a visual study
Inserted code (HTML)
- This code is automatically inserted into the page HTML for single sketch studies only.
- Variable 'dataPrice' contains the JSON data for price volume.

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
var dataPrice = [];
dataPrice[i] = getJsonData('##JSON_DATA_FILES##'); // Line per file
</script>
```

## Visual studies in this repository for this data-domain
 
* [Area Chart (D#.js)](#d3-area)
* [Correlation Turnover (D3.js)](#d3-correlation)
* [Line with Volume (D3.js)](#d3-linevol)
* [Standardised Close (D3.js)](#d3-standardclose)
* [Monthly Dimensional (DC.js)](#dC-monthdim)
* [Line Chart (dygraph.js)](#dygraph-line)

## <a name="d3-area"></a>Visual Study: Area Chart (D3)

![stator_d3area](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-price-time-d3.png?raw=true)

## <a name="d3-correlation"></a>Visual Study: Correlation Turnover (D3)

![stator_d3cor](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-correlationturnover-d3.png?raw=true)

## <a name="d3-linevol"></a>Visual Study: Line with Volume (D3)

![stator_d3linvol](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-line-volume-d3.png?raw=true)

## <a name="d3-standardclose"></a>Visual Study: Standardised Close (D3)

![stator_d3stan](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-standardclose-d3.png?raw=true)

## <a name="dC-monthdim"></a>Visual Study: Monthly Dimensional (DC)

![stator_dcmondim](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-month-dimension-dc.png?raw=true)

## <a name="dygraph-line"></a>Visual Study: Line (dygraph)

![stator_dylin](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_markets-charting-line-dygraph.png?raw=true)

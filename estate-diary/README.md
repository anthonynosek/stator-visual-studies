## Data Domain: Estate-Diary
Stator AFM (Visual Studies)

### Domain explanation
Display diary notes saved against:
- Estate
- Pending Position
- Open Position
- Closed Position Event.

### Where are canvases for this domain found within Stator?
1. **Estate - Diary Notes**  
   From the main Stator screen open an Estate, select "Diary Notes".

### JSON data format
- Data is represented by the following JSON.
- Newlines are represented by the character sequence '\r\n'.
- Date is in yyyy-MM-dd HH:mm:ss format (HH = 24 hour notation).
- OriginTypeName indicates the origin type for the diary note (estate, pending, open, closed position).

```json
[
    {
        "UniqueIdentifier": null,
        "Type": {
            "Description": "General"
        },
        "NoteDate": "2013-08-24 14:00:00",
        "NoteText": "This is a diary note saved for an estate. Newlines are indicated by the character sequence \r\n.",
        "Attachment": "",
        "AttachmentDescription": "",
        "CreatedDate": "2013-08-26 04:14:24",
        "OriginTypeName": "Estate",
        "OriginDescription": "Estate: William Burroughs"
    },
    {
        "UniqueIdentifier": null,
        "Type": {
            "Description": "Position"
        },
        "NoteDate": "2013-08-25 14:00:00",
        "NoteText": "Diary note assigned to a pending position.",
        "Attachment": "",
        "AttachmentDescription": "",
        "CreatedDate": "2013-08-26 07:15:13",
        "OriginTypeName": "Position Pending",
        "OriginDescription": "Pending Position\r\n1,000 BHP (AUD) @ 32.30\r\nEntry Date: 22/08/2013"
    },
    {
        "UniqueIdentifier": null,
        "Type": {
            "Description": "News"
        },
        "NoteDate": "2013-08-25 14:00:00",
        "NoteText": "Diary note assigned to an open position.",
        "Attachment": "",
        "AttachmentDescription": "",
        "CreatedDate": "2013-08-26 04:58:15",
        "OriginTypeName": "Open Position",
        "OriginDescription": "Open Position\r\n300 DES (USD) @ 10.00\r\nEntry Date: 25/08/2013"
    },
    {
        "UniqueIdentifier": null,
        "Type": {
            "Description": "General"
        },
        "NoteDate": "2013-08-25 14:00:00",
        "NoteText": "Diary note assigned to a closed position event.",
        "Attachment": "",
        "AttachmentDescription": "",
        "CreatedDate": "2013-08-26 07:14:32",
        "OriginTypeName": "Position Closed",
        "OriginDescription": "Closed Position Event\r\nGE (USD)\r\nExit Price: 23.40\r\nExit Date: 26/08/2013\r\n"
    }
]
```

### Accessing the data from a visual study
Inserted code (HTML)
- This code is automatically inserted into the page HTML for single sketch studies only.
- Variable 'dataDiary' contains the JSON data for the diary notes.

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
var dataDiary = getJsonData('##JSON_DATA_FILE##');
</script>
```

## Visual studies in this repository for this data-domain

* [Diary notes calendar grid (D#.js)](#d3-grid)

## <a name="d3-grid"></a>Visual Study: Diary Notes Calendar Grid (D3)

![stator_d3grid](https://raw.githubusercontent.com/anthonynosek/stator-visual-studies/master/_misc/graphics/screen_estate-diary-by-calendar-d3.png?raw=true)

(Above) Diary notes calendar grid layout. A calendar for the current and penultimate year is displayed as a grid. Squares in the grid are coloured based upon the frequency of diary notes occurring on each day. The colour depth is related to the frequency as shown by the key. Hovering over a coloured grid will display the most recently occurring diary note below the calendar grid (as shown). Visualisation created using Data Driven Documents, D3.js and Stator.  
Author: Anthony Nosek

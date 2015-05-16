# Line Graphs
***
## HTML
The html structure is pretty simple. The gist of it is basically to create the structure of the page and load our js and styles.

## Load Data
We're loading data through d3, starting by loading text with d3.text() and then parsing it with d3.csv.parseRows().

```
var countries_regions = {};
d3.text('country-regions.csv', 'text/csv', function(text) {
    var regions = d3.csv.parseRows(text);
    for (i=1; i < regions.length; i++) {
        countries_regions[regions[i][0]] = regions[i][1];
    }
});
```

# sri

1.Charts & Maps

Add a div in your webpage. Give it an id and set a specific width and height which will be the width and height of your chart.
<div id="container" style="width:100%; height:400px;"></div>
 
A chart is initialized by adding the JavaScript tag, <script> </script>, anywhere in a webpage, containing the following code for jQuery. The div from #1 is referenced in the jQuery object.
$(function () { 
    var myChart = Highcharts.chart('container', {
        chart: {
            type: 'bar'
        },
        title: {
            text: 'Fruit Consumption'
        },
        xAxis: {
            categories: ['Apples', 'Bananas', 'Oranges']
        },
        yAxis: {
            title: {
                text: 'Fruit eaten'
            }
        },
        series: [{
            name: 'Jane',
            data: [1, 0, 4]
        }, {
            name: 'John',
            data: [5, 7, 3]
        }]
    });
});
The code above uses the jQuery specific way of launching code on document ready, as explained at the jQuery website.

If you are inserting a Stock chart, there is a separate constructor method called Highcharts.StockChart. In these charts, typically the data is supplied in a separate JavaScript array, either taken from a separate JavaScript file or by an Ajax call to the server.

var chart1; // globally available
$(function() {
       chart1 = Highcharts.stockChart('container', {
         rangeSelector: {
            selected: 1
         },
         series: [{
            name: 'USD to EUR',
            data: usdtoeur // predefined JavaScript array
         }]
      });
   });
You should now see this chart on your webpage:


Optionally, you can apply a global theme to your charts. A theme is just a set of options that are applied globally through the Highcharts.setOptions method. The download package comes with four predefined themes. To apply a theme from one of these files, add this directly after the highcharts.js file inclusion:
<script type="text/javascript" src="/js/themes/gray.js"></script>


2. Parsing JSON data and Clearing existing dropdown list and loading the new JSON data with it. - Named as  Parsing Json Lists in DropDowns

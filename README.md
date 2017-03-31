# Google Dashboard
Connect and display Google Sheets data as a web-based dashboard with controls (cfr. https://developers.google.com/chart/interactive/docs/gallery/controls#dashboard).

## Google Apps Script ##
* Tutorial: Building a Charts Dashboard https://developers.google.com/apps-script/articles/charts_dashboard
  * It uses UiApp Class (https://developers.google.com/apps-script/reference/ui/ui-app) that is **deprecated**; 
  Google suggests using HTML Service instead (https://developers.google.com/apps-script/guides/html/)
  * It uses the Charts Class (https://developers.google.com/apps-script/reference/charts/charts) that it is not defined when using HTML Service
* ChartWrapper Class (https://developers.google.com/chart/interactive/docs/reference#chartwrapper-class)
  * all options can be specified either inline in the constructor (e.g. `'containerId': 'chart_div',`) or with associated methods (e.g. `setContainerId(chart_div)`)
  * all chart types https://developers.google.com/chart/interactive/docs/gallery
  
## Examples ##
* Simple chart (no dashboard with controls) https://gist.github.com/bennettscience/c314a9251cb4f4661adac95c517d31c5

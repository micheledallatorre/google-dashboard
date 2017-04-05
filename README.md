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
* Using Boostrap https://codepen.io/flopreynat/pen/BfLkA
* Build a Charts Dashboard with Google Sheets and HTML Service https://ctrlq.org/code/20094-google-charts-dashboard-with-google-sheets

## Instructions ##
Based on https://ctrlq.org/code/20094-google-charts-dashboard-with-google-sheets.

### Code.gs file ###

```JavaScript
// Code.gs file in Google App Scripts
function doGet(e) { 
  return HtmlService
  .createTemplateFromFile("index")
  .evaluate()
  .setTitle("Google Spreadsheet Chart")
  .setSandboxMode(HtmlService.SandboxMode.IFRAME);
}

function getSpreadsheetData() {
  var ssID   = "1dKEgrMoLJyF2AcL3gKx-vM_fmHLWMyJKI0E_xW3aMpo",
      sheet  = SpreadsheetApp.openById(ssID).getSheets()[0],
      data   = sheet.getDataRange().getValues();
  
  // use this to show data in the Logger console in Google App Scripts 
  //Logger.clear();
  //Logger.log(data);
  
  return data;    
}
```

### index.html file ###

```HTML
TODO
```


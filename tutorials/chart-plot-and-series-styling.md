# Chart Plot & Series Styling

### Overview

While ZingChart provides default styling themes for all of our chart types, most users want to modify the appearance to better meet the needs of their individual projects. It is in the `"plot"` and `"series"` objects that you apply attributes to change the styling of data points on your chart. These changes can be applied to affect a single series or the entire series array. We also offer the functionality to style by node or individual data points. Finally, this tutorial explains the different state types, or how data can appear under different conditions \(when data points are hovered over, selected, and so on\).  


```javascript
"plot": {
  //For global styling, place styling attributes here.
},
"series": [
  {
    "values": [y0, y1, y2, y3, ..., yN],
      //For local styling, place styling attributes here.
  },
  ...
]
```



<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribute</th>
      <th style="text-align:left">Type</th>
      <th style="text-align:left">Info</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">data</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">
        <p>The new configuration data.</p>
        <p>{...}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">graphid</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The ID of the graph object.</p>
        <p>&quot;mygraph&quot; | 0 | 1 | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The ID of the zingchart object.</p>
        <p>&quot;mychart&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">object</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">The object to modify if set in the API call.</td>
    </tr>
  </tbody>
</table>
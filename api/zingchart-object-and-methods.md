---
description: test
---

# ZingChart Object and Methods

### Overview

The ZingChart object contains properties to set global attributes such as general font face or size. The object also contains three important methods: the render method \(`zingchart.render()`\), which controls the rendering formats and characteristics to display the chart; the exec method \(`zingchart.exec()`\), which provides a mechanism to invoke various API calls on a chart; and the bind \(`zingchart.bind()`\) and unbind \(`zingchart.unbind()`\) methods, which listen for events that occur in the chart, and then do something with that event.  


### ZingChart Object

The ZingChart object contains the necessary properties and methods for chart rendering.

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
      <td style="text-align:left">ASYNC</td>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">
        <p>Renders the chart in &quot;steps&quot;, providing faster (but incremental)
          visual results. This is useful in case of big charts that take longer time
          to render.</p>
        <p>true | false | 1 | 0</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://www.zingchart.com/docs/api/zingchart-object/#api-events-bind-method">bind</a>
      </td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">
        <p>Binds an event to a chart (or to all charts in a page).</p>
        <p>zingchart.bind(&quot;id&quot;, &quot;eventName&quot;, function() {...})</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://www.zingchart.com/docs/api/zingchart-object/#api-methods">exec</a>
      </td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">
        <p>The API entry method, used to call various API commands against the chart.</p>
        <p>zingchart.exec(&quot;id&quot;, &quot;call&quot;, {...})</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">FONTFAMILY</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Global setting for the font family used by all the elements of the library.</p>
        <p>&quot;Arial&quot; | &quot;Helvetica&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">FONTSIZE</td>
      <td style="text-align:left">Numeric</td>
      <td style="text-align:left">
        <p>Global setting for the font size used by all the elements of the library.</p>
        <p>9 | 11 | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">MODULESDIR</td>
      <td style="text-align:left"></td>
      <td style="text-align:left"></td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://www.zingchart.com/docs/api/zingchart-object/#render-method">render</a>
      </td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">Main rendering method.</td>
    </tr>
    <tr>
      <td style="text-align:left"><a href="https://www.zingchart.com/docs/api/zingchart-object/#api-events-unbind-method">unbind</a>
      </td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">
        <p>Unbinds an event from a chart (or from all charts in a page).</p>
        <p>zingchart.bind(&quot;id&quot;, &quot;eventName&quot;, function() {...})</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">ZCOUTPUT</td>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">
        <p>Sets whether an optional parameter called zcoutput, containing the rendering
          option, will be passed for every data request.</p>
        <p>true | false | 1 | 0</p>
      </td>
    </tr>
  </tbody>
</table>### Methods

The ZingChart object has various methods, specifically the render method, exec method \(for API methods\), and bind and unbind methods \(for API events\).

#### Render Method

The ZingChart render method is used to set various chart render options. At a minimum, you must specify the `id`and `data` elements for the chart to properly render and display.

```javascript
zingchart.render({ 
  id : 'myChart', 
  data : { ... }, 
  height: 400, 
  width: 600 
});
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
      <td style="text-align:left">auto-resize
        <br />autoResize</td>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">true | false | 1 | 0</td>
    </tr>
    <tr>
      <td style="text-align:left">background-color
        <br />backgroundColor</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;none&quot; | &quot;transparent&quot; | &quot;#f00&quot; | &quot;#f00
        #00f&quot; | &quot;red yellow&quot; | &quot;rgb(100, 15, 15)&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">bgcolor</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;none&quot; | &quot;transparent&quot; | &quot;#f00&quot; | &quot;#f00
        #00f&quot; | &quot;red yellow&quot; | &quot;rgb(100, 15, 15)&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">border-color
        <br />borderColor</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;none&quot; | &quot;transparent&quot; | &quot;#f00&quot; | &quot;#f00
        #00f&quot; | &quot;red yellow&quot; | &quot;rgb(100, 15, 15)&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">border-width
        <br />borderWidth</td>
      <td style="text-align:left">Numeric</td>
      <td style="text-align:left">
        <p>To set the width of the chart.</p>
        <p>1 | 5 | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">cache</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">{ data: true | false defaults: true | false css: true | false csv: true
        | false }</td>
    </tr>
    <tr>
      <td style="text-align:left">cache-control
        <br />cacheControl</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;http-headers&quot; | &quot;query-string&quot; | &quot;none&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">color</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;none&quot; | &quot;transparent&quot; | &quot;#f00&quot; | &quot;#f00
        #00f&quot; | &quot;red yellow&quot; | &quot;rgb(100, 15, 15)&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">container</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;mydiv_id&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">csvdata</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;...&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">customprogresslogo</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>Allows user to specify what image appears on the loading screen, in lieu
          of the default ZingChart logo. Refer to our documentation on <a href="https://www.zingchart.com/docs/faq/removing-zingchart-branding/">Removing ZingChart Branding</a> for
          more information.</p>
        <p>&quot;image.png&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">data</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">
        <p>The chart data. For the chart to properly render, this and the <code>id</code> element
          are required.</p>
        <p>{...}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">dataurl</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;myjson.php&quot; | &quot;http://www.domain.com/myjson.php&quot;
        | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">defaults</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">{...}</td>
    </tr>
    <tr>
      <td style="text-align:left">defaultsurl</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;mydefaults.php&quot; | &quot;http://www.domain.com/mydefaults.php&quot;
        | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">events</td>
      <td style="text-align:left">Object</td>
      <td style="text-align:left">{ complete: function(p) { ... } load: function(p) { ... } ... }</td>
    </tr>
    <tr>
      <td style="text-align:left">exportdataurl</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;dataexportscript.php&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">exportimageurl</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;imageexportscript.php&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">fullscreen</td>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">true | false | 1 | 0</td>
    </tr>
    <tr>
      <td style="text-align:left">height</td>
      <td style="text-align:left">Mixed</td>
      <td style="text-align:left">
        <p>To set the height of the chart.</p>
        <p>300 | &quot;100%&quot; | &quot;auto&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">hideprogresslogo</td>
      <td style="text-align:left">Boolean</td>
      <td style="text-align:left">
        <p>To hide or remove the ZingChart logo that appears on the loading screen
          (generally only visible on charts with larger data sets). Refer to our
          documentation on <a href="https://www.zingchart.com/docs/faq/removing-zingchart-branding/">Removing ZingChart Branding</a> for
          more information.</p>
        <p>true | false | 1 | 0</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The element in the HTML document where you want the chart to render. For
          the chart to properly render, this and the <code>data</code> element are
          required.</p>
        <p>&quot;mydiv_id&quot;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">locale</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;en_us&quot; | &quot;fr&quot; | &quot;es&quot; | ...</td>
    </tr>
    <tr>
      <td style="text-align:left">output</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">&quot;canvas&quot; | &quot;svg&quot; | &quot;vml&quot; | &quot;auto&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left">width</td>
      <td style="text-align:left">Mixed</td>
      <td style="text-align:left">300 | &quot;100%&quot; | &quot;auto&quot; | ...</td>
    </tr>
  </tbody>
</table>### API Methods

**Exec Method**

The API entry method, used to call various API commands against the chart.

```text
zingchart.exec(id,'apicall',{
 ... options ...
});
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
      <td style="text-align:left">apicall</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The name of the API call.</p>
        <p>&quot;reload&quot; | &quot;resize&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The ID of the chart.</p>
        <p>&quot;mydiv&quot; | ...</p>
      </td>
    </tr>
  </tbody>
</table>### API Events

The bind and unbind methods are used with API events, allowing you to listen for events that happen in the chart \(e.g., node mouseover, node click\), and then doing something with that event. Refer to our documentation on [API Events](https://www.zingchart.com/docs/api/events/) for more information.

**Bind Method**

Binds an event to a chart \(or to all charts in a page\).

```javascript
zingchart.bind('id','eventName',function(event){ 
  ... event.value ...
});
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
      <td style="text-align:left">eventName</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The name of the event.</p>
        <p>&quot;load&quot; | &quot;complete&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">handler</td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">
        <p>Handler fired when the event takes place.</p>
        <p>function(params) {...}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The ID of the chart or null if event is bound to all the charts in a page.</p>
        <p>&quot;mydiv&quot; | null | ...</p>
      </td>
    </tr>
  </tbody>
</table>**Unbind Method**

Unbinds an event from a chart \(or from all charts in a page\).

```javascript
zingchart.unbind('id','eventName',function(event){ 
  ... event.value ...
});
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
      <td style="text-align:left">eventName</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The name of the event.</p>
        <p>&quot;load&quot; | &quot;complete&quot; | ...</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">handler</td>
      <td style="text-align:left">Function</td>
      <td style="text-align:left">
        <p>Handler fired when the event takes place.</p>
        <p>function(params) {...}</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">String</td>
      <td style="text-align:left">
        <p>The ID of the chart or null if event is bound to all the charts in a page.</p>
        <p>&quot;mydiv&quot; | null | ...</p>
      </td>
    </tr>
  </tbody>
</table>Got a question about how the ZingChart object and its methods work? We are happy to help. Email [support@zingchart.com](mailto:support@zingchart.com) or start a chat right here on this page for help.  
  



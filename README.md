# finalproject
Data Source: https://worldpopulationreview.com/state-rankings/mental-health-statistics-by-state

### Major Functions
``` HTML
function highlightFeature(e) {
  var layer = e.target;
layer.setStyle({
                  weight: 8,
                  opacity: 0.8,
                  color: '#e3e3e3',
                  fillColor: '#DDA0DD',
                  fillOpacity: 0.5
                  });
layer.bringToFront();

  info.update(layer.feature.properties);
                  }

function resetHighlight(e) {
                  geojson.resetStyle(e.target);
                  info.update();  
                  }

function zoomToFeature(e) {
                  map.fitBounds(e.target.getBounds());
                  }
  function onEachFeature(feature, layer) {
                  layer.on({
                  mouseover: highlightFeature,
                  click: zoomToFeature,
                  mouseout: resetHighlight
                  });
                  }
```

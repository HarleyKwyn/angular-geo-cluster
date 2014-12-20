angular-geo-cluster
===================

Geo-clustering d3 directive for angular. 

##There's no tests?!
Please see this article about testing with D3
http://pivotallabs.com/d3-test-driven-development/

This is a great starting point for a geo-cluster graph.

##Get Started

**(1)** include these dependencies on your page
```html
<script src="//cdnjs.cloudflare.com/ajax/libs/d3/3.4.11/d3.min.js"></script>
<script src="//cdnjs.cloudflare.com/ajax/libs/topojson/1.1.0/topojson.min.js"></script> 
```
**(2)** `npm install angular-geo-cluster --save` or `bower install angular-geo-cluster --save` 

**(3)** include the directive in your app
```
<div geo-cluster 
  data="data" 
  zoom="zoomStateParamtere" 
  centroids="centroidsOfClusters" 
  hover="hoverActionForCluster">
</div >
```

##Parameters
 * data: An array data objects that have a 'coords' key with an array containing the latitude and longitude of that data point.
 * zoom: An integer representing the current zoom level of the visualization.
 * centroids: An array of coordinate arrays of the centroids of the clustered data in latitude and longitude. 
 * hover: A function that is called when a centroid is hovered over. Allows for displaying data in that cluster. And gives you access to the current data in that cluster.

##Clustering
You will have to use your own clustering algorithm. There are some great k-means ones out there and I plan to package my own that's written in JavaScript but generally speaking clustering algorithms are processor intensive and may be something you want to cache so this could be done through and API as well.


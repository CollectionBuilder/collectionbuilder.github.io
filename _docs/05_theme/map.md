---
title: Map Page
stub: map
section: theme
section_order: 7
---

{:.py-4 .mt-4 #map}
*** 

<div class="row" markdown="1">
## Map Page

{% include bootstrap/image.md img="/theme/map.jpg" %}

- **latitude**: Determines the center of map.
	- example --> `latitude: 46.727485 `

- **longitude**: Determines the center of map.
	- example --> `longitude: -117.014185`

- **zoom-level**: Determines the zoom level for your map. The higher the number, the more zoomed-in you'll be. 
	- Range: any whole number between [`0` - `18`]
	- example --> `zoom-level: 5`

**The fields below determine *map search* and *map cluster* features. For larger collections with many items at one spot, we recommend turning on the map-cluster option and turning off the map-search feature.**

<div class="col-md-8" markdown="1">
- **map-search**: Enables a user to search the map via the large magnifying glass on the top right. 
	- Not suggested for large collections.
	- Options: `true`, `false`
	- example --> `map-search: true`

- **map-search-fuzziness**: Allows for less precision with search terms. 
	- Range:
		- `0` = exact match only
		- `1` = anything
	- example --> `map-search-fuzziness: 0.35`

- **map-cluster**: Clusters markers that are near each other.
	- Suggested for large collections or for collections with many items in same location.
	- Options: `true`, `false`
	- example --> `map-cluster: true`

- **map-cluster-radius**: Determines the size of clusters
	- Range: `10` to `80`
	- example --> `map-cluster-radius: 25`
</div>

<div class="col-md-4" markdown ="1">
{% include bootstrap/alert.md color="info" text="**Tip:** A user can change the **layer** the map is using by clicking on the Layer button at the top right of the map in the browser. 

The map can be **searched** by clicking on the magnifying glass just below the layers option at the top right." %}
</div>
</div>

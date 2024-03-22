# No-Utility-Network
GIS scripts for ESRI software

In migrating from ArcMap to ArcGIS Pro, we're being forced to migrate away from our geometric networks.  
Utility Network will require a huge schema change that will cost us time and money.  
Since we only used the most basic of functionality in geometric networks, we've decided to move forward with a No Network solution.

We'll be using Map Topology in ArcGIS Pro to facilitate moving coincident items during editing.

The one piece of missing functionality we've come to depend on to keep our data "connected" is the geometric network junctions, which show up on the ends of any line feature that doesn't already have a point feature there.
And then when a point is placed on top of a junction, the junction disappears.

These two Attribute Rules re-create that functionality in an ArcPro environment.  

# Installation:
* Create a point feature class to act as junctions.  If you're migrating from an existing geometric network, I recommend making it the same name for map continuity.
* Create a new attribute rule on each line and point feature class you want to participate in the fake network.  
* Update the contents of each rule to match your feature class names

# No Utility Network - junctions

## Background
In migrating from ArcMap to ArcGIS Pro, we're being forced to migrate away from our geometric networks.  Utility Network would require a huge schema change that would cost us time and money.  Since we only used the most basic of functionality in geometric networks, we've decided to move forward with a No Network solution.

We'll be using Map Topology in ArcGIS Pro to facilitate moving coincident items together during editing.

## Use Case
The one piece of missing functionality we've come to depend on to keep our data "connected" is the geometric network junctions, which show up on the ends of any line feature that doesn't already have a point feature there. When a point is placed on top of a junction, the junction disappears.  Additionally when a point on a line is deleted, a junction is added.

These three Attribute Rules re-create that functionality in an ArcPro environment.  

## Installation:
* Create a point feature class to act as junctions.  If you're migrating from an existing geometric network, I recommend making it the same name for map continuity.
* Create a new attribute rule on each line and two attribute rules each point feature class that you want to participate in the fake network.  
* Update the Arcade code of each rule to match your feature class names

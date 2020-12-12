---
id: Stitch-Shapes
title: Stitch Shapes
---

## Code Snippet
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->

```python
stitch_side1 = BwApi.StitchSide(from_shape, from_edge, 0, 100) 
stitch_side2 = BwApi.StitchSide(to_shape, to_edge, 0, 100)  
# Create a new stitch
BwApi.StitchCreate(BwApi.GarmentID(), stitch_side1, stitch_side2)
```
<!--C++-->

```cpp
// Create a new stitch
BwApiStitchCreate(garmentId, side1, side2);
```
<!--C#-->

```csharp
// Create a new stitch
BwApi.StitchCreate(garmentId, side1, side2);
```
<!--END_DOCUSAURUS_CODE_TABS-->
<br/>

## Result
![](../assets/stitch-shapes/stitch.png)
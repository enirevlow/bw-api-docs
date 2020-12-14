---
id: Costing
title: Costing
---
## Get surface area material
### Code snippet

<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
BwApi.MaterialSurfaceAreaGet(garmentId, colorwayId, materialId, sizeId)
```
<!--C++-->
```cpp
float area;
BwApiMaterialSurfaceAreaGet( garmentId, colorwayId, materialId, sizeId, &area);
```
<!--C#-->
```csharp
float area;
BwApi.MaterialSurfaceAreaGet(garmentId, colorwayId, materialId, sizeId, out area);
```
<!--END_DOCUSAURUS_CODE_TABS-->
<br/>

### Result
The surface area of a material. <br/>

## Get length material
### Code snippet

<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
# get an existing material length and depth (works only on lines and seams)
length, depth = BwApi.MaterialLengthGet(garmentId, colorwayId, materialId, sizeId)
```
<!--C++-->
```cpp
// get an existing material length and depth (works only on lines and seams)
float length;
float depth;
BwApiMaterialLengthGet( garmentId, colorwayId, materialId, sizeId, &length, &depth);
```
<!--C#-->
```csharp
// get an existing material length and depth (works only on lines and seams)
float length;
float depth;
BwApi.MaterialLengthGet(garmentId, colorwayId, materialId, sizeId, out length, out depth);
```
<!--END_DOCUSAURUS_CODE_TABS-->
<br/>

### Result
The length and depth of a material.
---
id: Assign-Material
title: Assign Material
---

## Assign fabric

### Code Snippet
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
BwApi.ShapeMaterialIdSet(garmentId, shapeId, materialId)
```
<!--C++-->
```cpp
BwApiShapeMaterialIdSet(garmentId, shapeId, materialId);
```
<!--C#-->
```csharp
BwApiShapeMaterialIdSet(garmentId, shapeId, materialId);
```
<!--END_DOCUSAURUS_CODE_TABS-->

<br/>

### Result
![](../assets/assign-material/assign-fabric.png)

## Assign seam

### Code Snippet
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
BwApi.EdgeMaterialIdSet(garmentId, shapeId, edgeId, materialId)
```
<!--C++-->
```cpp
BwApiEdgeMaterialIdSet(garmentId, shapeId, edgeId, materialId);
```
<!--C#-->
```csharp
BwApiEdgeMaterialIdSet(garmentId, shapeId, edgeId, materialId);
```
<!--END_DOCUSAURUS_CODE_TABS-->

<br/>

### Result
![](../assets/assign-material/assign-seam.png)
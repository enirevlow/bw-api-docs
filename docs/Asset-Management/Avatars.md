---
id: Avatars
title: Avatars
---
Avatars is what you dress the garments on 3D. Use the Avatars API get the current avatar, set the current avatar, get the list of all the avatars in VStitcher/Lotta, and so on.

For more information about the feature, please visit <a href="https://support.browzwear.com/VStitcher/Avatars/avatars.htm" target="_blank">here</a>.

To learn more about the rest of the Avatar API, please refer to <a href="https://gitlab.com/browzwear/share/open-platform/client-api/-/blob/master/BWPlugin/include/General/BWPluginAPI_Avatar.h" target="_blank">Avatar</a> in the repository.

## Sample plugin
Sample plugin for Avatars is available <a href="https://gitlab.com/browzwear/share/open-platform/client-api/-/tree/master/sample-plugins/python/Avatar" target="_blank">here</a>

## Getting current avatar 

### Code snippet

<br/>
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
current_avatar_id = BwApi.AvatarCurrentGet()
```
<!--C++-->
```cpp
BwApiString* avatarId = BwApiStringCerate();
BwApiAvatarCurrentGet(avatarId);
```
<!--C#-->
```csharp
string avatarId;
BwApi.AvatarCurrentGet(out avatarId);
```
<!--END_DOCUSAURUS_CODE_TABS-->

<br/>

### Result
The id of the current avatar

## Importing an avatar

### Code snippet

Note: the avatar file must be FBX, OBJ, or AVA.
<br/>
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
# assuming the path is valid and the file format is valid
avatarId = BwApi.AvatarImport(path)
```
<!--C++-->
```cpp
// assuming the path is valid and the file format is valid
BwApiString* avatarId = BwApiStringCreate();
BwApiAvatarImport(path, avatarId);
```
<!--C#-->
```csharp
string avatarId;
BwApi.AvatarImport(path, out avatarId);
```
<!--END_DOCUSAURUS_CODE_TABS-->

<br/>

### Result
![](../assets/Avatar/import-avatar.PNG)

## Importing a VSA file

### Code snippet

<br/>
<!--DOCUSAURUS_CODE_TABS-->

<!--Python-->
```python
# assuming the path is valid and the file format is valid
avatarIds = BwApi.AvatarImportVSA(path)
```
<!--C++-->
```cpp
// assuming the path is valid and the file format is valid
BwApiVectorString* avatarIds = BwApiVectorStringCreate();
BwApiAvatarImportVSA(path, avatarIds);
```
<!--C#-->
```csharp
BwApiVectorString avatarIds = new BwApiVectorString();
BwApi.AvatarImportVSA(path, out avatarIds);
```
<!--END_DOCUSAURUS_CODE_TABS-->

<br/>

### Result
![](../assets/Avatar/import-avatar.PNG)

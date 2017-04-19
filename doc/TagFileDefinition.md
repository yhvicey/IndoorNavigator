# File define
a tag file is a xml file with a specified format.

# File example
```
<?xml version="1.0" encoding="utf-8"?>
<Tags Version="1.1">
    <Tag Floor="0" Type="GuideNode" Index="0" Value="Tag 1"/>
    <Tag Floor="0" Type="GuideNode" Index="1" Value="标签 2"/>
</Tags>
```
# Element defines

## Tags
Root element that contains tag elements.

|Attribute|Description|
|-|-|
|Version|Specify tag file's version.|

## Tag
Tag element. Representing a tag.

|Attribute|Description|
|-|-|
|Floor|Tag's floor.|
|Type|Tag's target node's type.|
|Index|Tag's target node's index.|
|Value|Tag's value.|
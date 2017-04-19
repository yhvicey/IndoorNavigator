# File define

a map file is a xml file with a specified format.

# File example

```
<?xml version="1.0" encoding="utf-8"?>
<Map Version="1.1" Name="物联网学院B区">
    <Floor>
        <GuideNode X="0" Y="10" Next="0" />
        <GuideNode X="100" Y="20" />
        <GuideNode X="70" Y="30" />
        <GuideNode X="50" Y="60" />
        <GuideNode X="50" Y="43" />
        <GuideNode X="45" Y="32" Name="b141" />
        <!-- More guide nodes here -->
        <WallNode X="20" Y="40" />
        <WallNode X="20" Y="50" />
        <WallNode X="40" Y="50" />
        <WallNode X="40" Y="40" />
        <!-- More wall nodes here -->
        <Link StartType="EntryNode" StartIndex="0" EndType="GuideNode" EndIndex="0" />
        <Link StartType="GuideNode" StartIndex="0" EndType="GuideNode" EndIndex="1" />
        <Link StartType="GuideNode" StartIndex="1" EndType="GuideNode" EndIndex="2" />
        <Link StartType="GuideNode" StartIndex="2" EndType="EntryNode" EndIndex="0" />
        <!-- More links here -->
    </Floor>
    <Floor>
        <GuideNode X="0" Y="10" Prev="0" />
        <GuideNode X="100" Y="20" />
        <GuideNode X="70" Y="30" />
        <GuideNode X="50" Y="60" />
        <GuideNode X="50" Y="43" />
        <GuideNode X="45" Y="32" Name="b241" />
        <WallNode X="20" Y="40" />
        <WallNode X="20" Y="50" />
        <WallNode X="40" Y="50" />
        <WallNode X="40" Y="40" />
        <Link StartType="EntryNode" StartIndex="0" EndType="GuideNode" EndIndex="0" />
        <Link StartType="GuideNode" StartIndex="0" EndType="GuideNode" EndIndex="1" />
        <Link StartType="GuideNode" StartIndex="1" EndType="GuideNode" EndIndex="2" />
        <Link StartType="GuideNode" StartIndex="2" EndType="EntryNode" EndIndex="0" />
    </Floor>
    <!-- More floors here -->
</Map>
```
# Element defines

## Map
Root element that contains floor elements.

|Attribute|Description|
|---|---|
|Version|Specify map file's version. Current version is 1.1.|
|Name|Map's name.|

## Floor
Floor element. Representing a floor, and contains node elements.

## Node
Base element for nodes. Contains its position and links.

|Attribute|Description|
|---|---|
|X|X position of the node in double. Start from 0.|
|Y|Y position of the node in double. Start from 0.|

### GuideNode
GuideNode element. Have optional Name attribute. if it is an entry, there will be optional Prev and Next attribute.

|Attribute|Description|
|---|---|
|Name|Node name.|
|Prev|Previous entry's index which is connected to this entry. Start from 0.|
|Next|Next entry's index which is connected to this entry. Start from 0.|

### WallNode
WallNode element. Contains its properties and links.

## Link
Link element. Representing a link from its parent node to target node.

|Attribute|Description|
|---|---|
|Type|Type of target node. Must be "EntryNode", "GuideNode" or "WallNode".|
|Index|Index of target node. Start from 0.|
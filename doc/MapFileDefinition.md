# Map file definition

## File define

A map file is a xml file with a specified format.

## File example

```XML
<?xml version="1.0" encoding="utf-8"?>
<Map Version="1.1" Name="物联网学院B区">
    <Floor>
        <Node Type="GuideNode" X="0" Y="10" Next="0" />
        <Node Type="GuideNode" X="100" Y="20" />
        <Node Type="GuideNode" X="70" Y="30" />
        <Node Type="GuideNode" X="50" Y="60" />
        <Node Type="GuideNode" X="50" Y="43" />
        <Node Type="GuideNode" X="45" Y="32" Name="b141" />
        <!-- More guide nodes here -->
        <Node Type="WallNode" X="20" Y="40" />
        <Node Type="WallNode" X="20" Y="50" />
        <Node Type="WallNode" X="40" Y="50" />
        <Node Type="WallNode" X="40" Y="40" />
        <!-- More wall nodes here -->
        <Link Type="GuideNode" StartIndex="0" EndIndex="0" />
        <Link Type="GuideNode" StartIndex="0" EndIndex="1" />
        <Link Type="GuideNode" StartIndex="1" EndIndex="2" />
        <Link Type="GuideNode" StartIndex="2" EndIndex="0" />
        <!-- More links here -->
    </Floor>
    <Floor>
        <Node Type="GuideNode" X="0" Y="10" Prev="0" />
        <Node Type="GuideNode" X="100" Y="20" />
        <Node Type="GuideNode" X="70" Y="30" />
        <Node Type="GuideNode" X="50" Y="60" />
        <Node Type="GuideNode" X="50" Y="43" />
        <Node Type="GuideNode" X="45" Y="32" Name="b241" />
        <Node Type="WallNode" X="20" Y="40" />
        <Node Type="WallNode" X="20" Y="50" />
        <Node Type="WallNode" X="40" Y="50" />
        <Node Type="WallNode" X="40" Y="40" />
        <Link Type="GuideNode" StartIndex="0" EndIndex="0" />
        <Link Type="GuideNode" StartIndex="0" EndIndex="1" />
        <Link Type="GuideNode" StartIndex="1" EndIndex="2" />
        <Link Type="GuideNode" StartIndex="2" EndIndex="0" />
    </Floor>
    <!-- More floors here -->
</Map>
```

## Element defines

### Map

Root element that contains floor elements.

|Attribute|Description|
|---|---|
|Version|Specified map file's version. Current version is 1.1.|
|Name|Map's name.|

### Floor

Floor element. Representing a floor, and contains node elements.

### Node

Node element. Reresenting a guidenode or wallnode.

|Attribute|Description|
|---|---|
|X|X position of the node in double. Start from 0.|
|Y|Y position of the node in double. Start from 0.|
|Type|Node type.|
|Name|Node name.|
|Prev|Previous entry's index which is connected to this entry. Start from 0.|
|Next|Next entry's index which is connected to this entry. Start from 0.|

### Link

Link element. Representing a link from its parent node to target node.

|Attribute|Description|
|---|---|
|Type|Type of target node. Must be "EntryNode", "GuideNode" or "WallNode".|
|StartIndex|Index of start node. Start from 0.|
|EndIndex|Index of end node. Start from 0.|
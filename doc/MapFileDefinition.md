# File define
a map file is a xml file with a specified format.
# File example
```
<?xml version="1.0" encoding="utf-8"?>
<Map Version="1.0" Name="物联网学院B区">
    <Floor>
        <EntryNode X="0.0" Y="10.0" Next="0">
            <Link Type="GuideNode" Index="0" />
        </EntryNode>
        <!-- More entry nodes here -->
        <GuideNode X="100.0" Y="20.0">
            <Link Type="GuideNode" Index="1" />
        </GuideNode>
        <GuideNode X="70.0" Y="30.0">
            <Link Type="GuideNode" Index="2" />
        </GuideNode>
        <GuideNode X="50.0" Y="60.0">
            <Link Type="EntryNode" Index="0" />
        </GuideNode>
        <GuideNode X="50.0" Y="43.0" />
        <GuideNode X="45.0" Y="32.0" Name="b141" />
        <!-- More guide nodes here -->
        <WallNode X="20.0" Y="40.0" />
        <WallNode X="20.0" Y="50.0" />
        <WallNode X="40.0" Y="50.0" />
        <WallNode X="40.0" Y="40.0" />
        <!-- More wall nodes here -->
    </Floor>
    <Floor>
        <Entry X="0.0" Y="10.0" Prev="0">
            <Link Type="GuideNode" Index="0" />
        </Entry>
        <GuideNode X="100.0" Y="20.0">
            <Link Type="GuideNode" Index="1" />
        </GuideNode>
        <GuideNode X="70.0" Y="30.0">
            <Link Type="GuideNode" Index="2" />
        </GuideNode>
        <GuideNode X="50.0" Y="60.0">
            <Link Type="EntryNode" Index="0" />
        </GuideNode>
        <GuideNode X="50.0" Y="43.0" />
        <GuideNode X="45.0" Y="32.0" Name="b241" />
        <WallNode X="20.0" Y="40.0" />
        <WallNode X="20.0" Y="50.0" />
        <WallNode X="40.0" Y="50.0" />
        <WallNode X="40.0" Y="40.0" />
    </Floor>
    <!-- More floors here -->
</Map>
```
# Element defines
## Map
Root element that contains floor elements.

|Attribute|Description|
|---|---|
|Version|Specified map file's version.|
|Name|Map's name.|

## Floor
Floor element. Representing a floor, and contains node elements.
## Node
Base element for nodes. Contains its position and links.

|Attribute|Description|
|---|---|
|X|X position of the node in double. Start from 0.|
|Y|Y position of the node in double. Start from 0.|

### EntryNode
EntryNode element. Have Name, Prev and Next attributes.

|Attribute|Description|
|---|---|
|Name|Node name.|
|Prev|Previous entry's index which is connected to this entry. Start from 0.|
|Next|Next entry's index which is connected to this entry. Start from 0.|

### GuideNode
GuideNode element. Have Name attribute.

|Attribute|Description|
|---|---|
|Name|Node name.|

### WallNode
WallNode element. Contains its properties and links.
## Link
Link element. Representing a link from its parent node to target node.

|Attribute|Description|
|---|---|
|Type|Type of target node. Must be "EntryNode", "GuideNode" or "WallNode".|
|Index|Index of target node. Start from 0.|
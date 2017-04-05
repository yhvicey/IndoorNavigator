# File define
a map file is a xml file with a specified format.
# File example
```
<?xml version="1.0" encoding="utf-8"?>
<Map Version="1.0" Name="物联网学院B区">
    <Floor>
        <Nodes>
            <Node X="0.0" Y="10.0" Type="Entry" NextEntry="0"/>
            <Node X="100.0" Y="20.0" Type="Guide"/>
            <Node X="70.0" Y="30.0" Type="Guide"/>
            <Node X="50.0" Y="60.0" Type="Guide"/>
            <Node X="50.0" Y="43.0" Type="Guide"/>
            <Node X="45.0" Y="32.0" Type="Guide" Name="b141"/>
            <Node X="20.0" Y="40.0" Type="Wall"/>
            <Node X="20.0" Y="50.0" Type="Wall"/>
            <Node X="40.0" Y="50.0" Type="Wall"/>
            <Node X="40.0" Y="40.0" Type="Wall"/>
            <!-- More nodes here -->
        </Nodes>
        <Links>
            <Link Start="0" End="1"/>
            <Link Start="1" End="2"/>
            <Link Start="2" End="3"/>
            <Link Start="3" End="0"/>
            <Link Start="0" End="1"/>
            <Link Start="1" End="2"/>
            <!-- More links here -->
        </Links>
    </Floor>
    <Floor>
        <Nodes>
            <Node X="0.0" Y="1.0" Type="Entry" PrevEntry="0"/>
            <Node X="10.0" Y="2.0" Type="Guide"/>
            <Node X="7.0" Y="3.0" Type="Guide"/>
            <Node X="5.0" Y="6.0" Type="Guide"/>
            <Node X="5.0" Y="4.3" Type="Guide"/>
            <Node X="4.5" Y="3.2" Type="Guide" Name="b141"/>
            <Node X="2.0" Y="4.0" Type="Wall"/>
            <Node X="2.0" Y="5.0" Type="Wall"/>
            <Node X="4.0" Y="5.0" Type="Wall"/>
            <Node X="4.0" Y="4.0" Type="Wall"/>
            <!-- More nodes here -->
        </Nodes>
        <Links>
            <Link Start="0" End="1"/>
            <Link Start="1" End="2"/>
            <Link Start="2" End="3"/>
            <Link Start="3" End="0"/>
            <Link Start="0" End="1"/>
            <Link Start="1" End="2"/>
            <!-- More links here -->
        </Links>
    </Floor>
    <!-- More floors here -->
</Map>
```
# Element defines
## Map
Root element that contains floor elements.
|Attribute|Description|
|-|-|
|Version|Specified .map file's version.|
|Name|Map's name.|
## Floor
Floor element. Representing a floor, and contains nodes element and links element.
## Nodes
Contains node elements.
## Node
Node element. Representing a node.
|Attribute|Description|
|-|-|
|X|X position of the node.|
|Y|Y position of the node.|
|Type|Type of the node. Must be "Entry", "Guide" or "Wall.|
|Name|Node name. Only valid on EntryNode and GuideNode.|
|PrevEntry|Previous entry connected to this entry. Only valid on EntryNode.|
|NextEntry|Next entry connected to this entry. Only valid on EntryNode.|
## Links
Contains link elements.
## Link
Link element. Representing a link between two nodes.
|Attribute|Description|
|-|-|
|Start|Index of start node.|
|End|Index of end node.|
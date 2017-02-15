# File define
a .map file is a xml file with a specified format.
# File example
```
<?xml version="1.0">
<Map Version="1.0">
    <Floors>
        <Floor Number="1">
            <Walls>
                <Wall StartAt="20.0, 40.0" EndAt="20.0, 50.0" />
                <Wall StartAt="20.0, 50.0" EndAt="40.0, 50.0" />
                <Wall StartAt="40.0, 50.0" EndAt="40.0, 40.0" />
                <Wall StartAt="40.0, 40.0" EndAt="20.0, 40.0" />
                <!-- More walls here -->
            </Walls>
            <Nodes>
                <Node At="100.0, 20.0" />
                <Node At="70.0, 30.0" />
                <Node At="50.0, 60.0" />
                <!-- More nodes here -->
            </Nodes>
        </Floor>
        <!-- More floors here -->
    </Floors>
</Map>
```
# Element defines
## Map
Main element that contains other elements such as map properties and floors.
|Attribute|Description|
|-|-|
|Version|Specified .map file's version.|
## Floors
Contains floor elements.
## Floor
Floor element. Representing a floor, and contains wall elements and node elements.
|Attribute|Description|
|-|-|
|Number|Number of the floor. Start from 1.|
||One number should only appear once in a file.|
||If not, the parsing will be broken.|
## Walls
Contains wall elements.
## Wall
Wall element. Representing a wall.
|Attribute|Description|
|-|-|
|StartAt|Start point of the wall.|
|EndAt|End point of the wall.|
## Nodes
Contains node elements.
|Attribute|Description|
|-|-|
|At|Position of the node.|
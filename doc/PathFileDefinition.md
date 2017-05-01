# File define
A path file is a xml file with a specified format.

# File example
```
<?xml version="1.0" encoding="utf-8"?>
<Path Version="1.0" Speed="100">
    <Node X="10" Y="10" />
    <Node X="20" Y="10" />
    <Node X="30" Y="10" />
    <Node X="40" Y="10" />
    <Node X="40" Y="20" />
    <Node X="40" Y="30" />
    <Node X="40" Y="40" />
</Path>
```
# Element defines

## Path
Root element that contains path node elements.

|Attribute|Description|
|---|---|
|Version|Specify tag file's version.|
|Speed|Emulating speed.|

## Node
Node element. Representing a path node.

|Attribute|Description|
|---|---|
|X|X position of the node in double. Start from 0.|
|Y|Y position of the node in double. Start from 0.|
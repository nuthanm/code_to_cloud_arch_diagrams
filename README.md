# Generating Diagrams with the Diagrams Library

## Overview

This repository contains Python code examples demonstrating how to generate diagrams using the Diagrams library.

## Prerequisites

Ensure you have the following prerequisites installed:

Python 3.6 or later

Graphviz (for rendering diagrams)

C++ Build Tools (if using Visual Studio 2022, choose the "Desktop development with C++" option)

## Installation

Install the required libraries using pip:
> pip install diagrams

## Examples

The following code examples illustrate various features of the Diagrams library:

### Program 1: Basic Diagram
```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram"):
    EC2("web")
```
### Program 2: Saving Diagram as Variable

```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram") as diag:
    EC2("web")
diag

```
### Program 3: Specifying Output Format
```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram", outformat="png"):  # Default format is PNG
    EC2("web")
```
### Program 4: Multiple Output Formats
```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram Multi Output", outformat=["jpg", "png", "dot"]):
    EC2("web")
```
### Program 5: Specifying Filename

```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram", filename="my_diagram"):
    EC2("web")
```
### Program 6: Disabling Immediate Rendering

```
from diagrams import Diagram
from diagrams.aws.compute import EC2

with Diagram("Simple Diagram", show=False):
    EC2("web")
```
### Program 7: Adjusting Graphviz Properties

```
from diagrams import Diagram
from diagrams.aws.compute import EC2

graph_attr = {
    "fontsize": "45",
    "bgcolor": "transparent"
}

with Diagram("Simple Diagram", show=False, graph_attr=graph_attr):
    EC2("web")
```

**Note:** All these you can find from official website with more details.

## Additional Information

Refer to the official Diagrams library documentation for more advanced usage and customization options: https://diagrams.mingrammer.com/
For GraphViz: https://www.graphviz.org/doc/info/attrs.html

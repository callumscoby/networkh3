<h1 align="left">networkh3</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.0.6-blue.svg?cacheSeconds=2592000" />
  <a href="#" target="_blank">
    <img alt="License: MIT License" src="https://img.shields.io/badge/License-MIT License-yellow.svg" />
  </a>
</p>

<p>A package to return clipped H3 hexagons from the extent of an OSMnx network. Useful for anyone looking to use the H3 spatial indexing system in route analyses or spatial analyses, and for saving time sourcing H3 hexagons.</p>

## Examples
<p>
<img src="https://raw.githubusercontent.com/callumscoby/networkh3/main/images/london_example.png" height="258px"/>
<img src="https://raw.githubusercontent.com/callumscoby/networkh3/main/images/beijing_example.png" height="258px" />
<img src="https://raw.githubusercontent.com/callumscoby/networkh3/main/images/washington_example.png" height="258px" />


<p>(L-R): London, Beijing, Sydney</p>

<p>Example workflows are available <a href="https://github.com/callumscoby/networkh3/tree/main/examples">here</a></p>

## Install

Install the latest version from PyPI:

```sh
pip install networkh3
```

## Import

```sh
from networkh3 import NETWORKH3
```

## Usage

NETWORKH3 requires three parameters: the area of interest, the type of OSMNx network, and the resolution of the returned H3 hexagons:

```sh
from networkh3 import NETWORKH3

NETWORKH3.get_h3('Leeds, United Kingdom', 'drive', 9, **kwargs)
```

Optional style keywords can also be specified:

```sh
from networkh3 import NETWORKH3
import contextily as cx

NETWORKH3.get_h3('Leeds, United Kingdom', 'drive', 9, 
                network_kwargs={
                  'node_size': 1, 
                  'node_color': 'black',
                  'edge_color': 'red',
                  'edge_linewidth': 0.2}, 
                h3_kwargs={
                  'facecolor': 'white', 
                  'alpha': 0.6}, 
                basemap_kwargs={
                  'source': cx.providers.Stamen.TonerLite}
                  )
```

## Issues and support

<p>Contribute or log issues <a href="https://github.com/callumscoby/networkh3/issues">here</a></p>

## Contact

* Website: <a href="https://callumscoby.com">callumscoby.com</a>
* Twitter: [@ScobyCallum](https://twitter.com/ScobyCallum)
* Github: [@callumscoby](https://github.com/callumscoby)
* LinkedIn: [@callumscoby](https://linkedin.com/in/callumscoby)

## Acknowledgements
* <p>⌇ <a href="https://github.com/gboeing/osmnx">OSMnx</a></p>

<!-- * ⌇ OSMnx (https://github.com/gboeing/osmnx) -->
* <p>🗺 <a href="https://github.com/uber/h3">H3</a></p>

<!-- * 🗺 H3 (https://github.com/uber/h3) -->

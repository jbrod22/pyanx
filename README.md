# pyanx

**Updated for Python 3**

This code is a fork of https://github.com/pcbje/pyanx and updated to work with Python 3.

This tool enables the generation chart files that can be opened in Analyst's Notebook. It's tested against I2 Chart Reader 8 (released May 2012) which is a free, read-only version of Analyst's Notebook. The generated chart files are on the Analyst's Notebook Exchange format (ANX).

I2 Chart Reader URL: https://www-304.ibm.com/connections/blogs/i2/entry/ibm_i2_chart_reader

#### Installation

`python setup.py install`

#### Usage

```
import pyanx

chart = pyanx.Pyanx()

tyrion = chart.add_node(entity_type='Person', label='Tyrion')
tywin = chart.add_node(entity_type='Person', label='Tywin')
jaime = chart.add_node(entity_type='Person', label='Jaime')
cersei = chart.add_node(entity_type='Woman', label='Cersei')

chart.add_edge(tywin, tyrion, 'Father of')
chart.add_edge(jaime, tyrion, 'Brother of')
chart.add_edge(cersei, tyrion, 'Sister of')

chart.create('demo.anx')
```

#### Output

<div align="center"><img src="https://raw.githubusercontent.com/pcbje/pyanx/master/test/anb_integration.png" width="600"/></div>

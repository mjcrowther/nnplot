# nnplot

Plot a schematic diagram of an artificial neural network in Stata.

`nnplot` draws a network with any number of inputs, outputs, hidden layers and nodes in each hidden layer. Every node in one layer is connected to every node in the next.

## Options

| Option | What it sets |
|---|---|
| `inputs(#)` | number of inputs; required |
| `outputs(#)` | number of outputs; required |
| `hlayers(#)` | number of hidden layers; the default is 1 |
| `hnodes(numlist)` | number of nodes in each hidden layer; the default is 1, and a single number applies to every hidden layer |
| `colors(list)` | colours to use for the layers |
| `inlabels(list)` | labels for the inputs; the default is `x#` |
| `outlabels(list)` | labels for the outputs; the default is `y#` |
| `hlabel(string)` | label for the hidden layers; the default is `Hidden layer` followed by its number |

## Installation

To install directly from this GitHub repository, use:

```stata
net install nnplot, from("https://raw.githubusercontent.com/mjcrowther/nnplot/main/")
```

## Example

A network with five inputs, one hidden layer of three nodes and one output:

```stata
nnplot, outputs(1) inputs(5) hlayers(1) hnodes(3)
```

The options are described in the help file: `help nnplot`.

## Version

Version 1.0.0 (3 February 2022).

## Licence

Copyright (C) 2022 Michael J. Crowther.

Released under the GNU General Public License, version 3. See [`LICENSE`](LICENSE).

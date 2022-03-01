# Pacman-dep-graph

[![License](https://img.shields.io/github/license/VincilLau/pacman-dep-graph)](https://github.com/VincilLau/pacman-dep-graph/blob/master/LICENSE)

`Pacman-dep-graph` can generate the dependency graph of installed pacman packages. When you run pacman-dep-graph, it will describe the dependency graph in `DOT language` and output it to `stdout`.

## Usage

```shell
git clone https://github.com/VicilLau/pacman-dep-graph.git
cd pacman-dep-graph
./pacman-dep-graph > pacman-dep-graph.dot
dot -Tpng pacman-dep-graph.dot -o pacman-dep-graph.png
```

For more infomation about `DOT language`, please visit [https://graphviz.org.](https://graphviz.org/)

## Maintainers

[@VincilLau.](https://github.com/VincilLau)

## License

[GPLv3](https://github.com/VincilLau/pacman-graph/blob/master/LICENSE) © Vincil Lau

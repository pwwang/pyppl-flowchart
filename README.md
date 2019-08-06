# pyppl-flowchart

[![Pypi][3]][4] [![Github][5]][6] [![PyPPL][7]][1] [![PythonVers][8]][4] [![Travis building][10]][11] [![Codacy][12]][13] [![Codacy coverage][14]][13]

Flowchart generator for [PyPPL](https://github.com/pwwang/PyPPL).

## Installation
```shell
pip install pyppl-flowchart
```

## Usage

### Generating flowchart for your pipeline
```python
# process definition

PyPPL().start(...).flowchart(fcfile = '/path/to/your/flowchart.svg').run()
```

### Hiding some processes from flowchart
```python
# Turn
# p1 -> p2 -> p3 -> p4 -> p5
p3.hide = True
# into:
# p1 -> p2 -> p4 -> p5
```

### Theming

In your configuration:
```yaml
default:
    _flowchart:
        theme: default
    # other default configurations
# other profiles
```

We have two builtin themes: `default` and `dark`:

![default](https://pyppl.readthedocs.io/en/latest/drawFlowchart_pyppl.png)

![dark](https://pyppl.readthedocs.io/en/latest/drawFlowchart_pyppl_dark.png)

You can also default your own theme in the configuration:
```yaml
default:
    _flowchart:
        theme:
            base:
                shape: box
                style: rounded,filled
                fillcolor: "#ffffff"
                color: "#000000"
                fontcolor: "#000000"
            start:
                style: filled
                color: "#259229"
            end:
                style: filled
                color: "#d63125"
            export:
                fontcolor: "#c71be4"
            skip:
                fillcolor: "#eaeaea"
            skip+:
                fillcolor: "#b5b3b3"
            resume:
                fillcolor: "#b9ffcd"
            resume+:
                fillcolor: "#58b773"
            procset:
                style: filled
                color: "#eeeeee"
```
[1]: https://github.com/pwwang/PyPPL
[2]: https://pyppl-flowchart.readthedocs.io/en/latest/
[3]: https://img.shields.io/pypi/v/pyppl-flowchart?style=flat-square
[4]: https://pypi.org/project/pyppl-flowchart/
[5]: https://img.shields.io/github/tag/pwwang/pyppl-flowchart?style=flat-square
[6]: https://github.com/pwwang/pyppl-flowchart
[7]: https://img.shields.io/github/tag/pwwang/pyppl?label=PyPPL&style=flat-square
[8]: https://img.shields.io/pypi/pyversions/pyppl-flowchart?style=flat-square
[10]: https://img.shields.io/travis/pwwang/pyppl-flowchart?style=flat-square
[11]: https://travis-ci.org/pwwang/pyppl-flowchart
[12]: https://img.shields.io/codacy/grade/6f03178e799d49458ff5dd5dbc81cacc?style=flat-square
[13]: https://app.codacy.com/project/pwwang/pyppl-flowchart/dashboard
[14]: https://img.shields.io/codacy/coverage/6f03178e799d49458ff5dd5dbc81cacc?style=flat-square

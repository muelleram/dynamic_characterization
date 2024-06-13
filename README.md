# dynamic_characterization

[![Read the Docs](https://img.shields.io/readthedocs/timex?label=documentation)](https://dynamic-characterization.readthedocs.io/en/latest/)
[![PyPI - Version](https://img.shields.io/pypi/v/dynamic-characterization?color=%2300549f)](https://pypi.org/project/dynamic-characterization/)
[![Conda Version](https://img.shields.io/conda/v/diepers/dynamic_characterization?label=conda)](https://anaconda.org/diepers/dynamic_characterization)
![Conda - License](https://img.shields.io/conda/l/diepers/bw_timex)

This is a collection of dynamic characterization functions for life cycle inventories with temporal information. The functions are meant to work with a common input format of the dynamic inventory, collected in a pandas DataFrame that looks like this:

| date | amount | flow | activity |
|-------|-------|------|----------|
| 101   | 33    | 1    | 2        |
| 312   | 21    | 4    | 2        |

The functions take one row of this dynamic inventory dataframe (i.e. one emission at one point in time) and transform it according to some metric. The output generated by applying a very simple function to both rows of the input dataframe could look like:

| date | amount | flow | activity |
|------|--------|------|----------|
| 101  | 33     | 1    | 2        |
| 102  | 31     | 1    | 2        |
| 103  | 31     | 1    | 2        |
| 312  | 21     | 4    | 2        |
| 313  | 20     | 4    | 2        |
| 314  | 19     | 4    | 2        |

## Installation

You can install `dynamic_characterization` via [pip] from [PyPI]:

```console
$ pip install dynamic_characterization
```

Alternatively, you can also use conda:

```console
$ conda install -c diepers dynamic_characterization
```

## Contributing

Contributions are very welcome.
To learn more, see the [Contributor Guide][Contributor Guide].

## License

Distributed under the terms of the [BSD 3 Clause license][License],
_dynamic_characterization_ is free and open source software.

## Issues

If you encounter any problems,
please [file an issue][Issue Tracker] along with a detailed description.


<!-- github-only -->

[command-line reference]: https://dynamic-characterization.readthedocs.io/en/latest/usage.html
[License]: https://github.com/TimoDiepers/dynamic_characterization/blob/main/LICENSE
[Contributor Guide]: https://github.com/TimoDiepers/dynamic_characterization/blob/main/CONTRIBUTING.md
[Issue Tracker]: https://github.com/TimoDiepers/dynamic_characterization/issues

# python-jsonlist

This module is used to read and write JSON-List files.

A JSON-List file is a text file that every line is a JSON string.

For example, a JSON-List file named test.jl has the following content:

    {"foo": "bar"}
    {"a": 123, "b": 456}

So that it can be loaded into python as a list of dicts:

    $ python3
    >>> import jsonlist
    >>> jsonlist.load_file('test.jl')
    [{'foo': 'bar'}, {'a': 123, 'b': 456}]

And a list of dicts can be dumped into a JSON-List file.

    $ python3
    >>> import jsonlist
    >>> jlist = [{'foo': 123, 'bar': 456}, {'hello': 'python'}, {}]
    >>> jsonlist.dump_file(jlist, 'output.jl')
    >>> exit()
    $ cat output.jl
    {"bar": 456, "foo": 123}
    {"hello": "python"}
    {}

## Requirements

python >= 3.3

## Installation

    python3 setup.py install


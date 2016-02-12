### Download Source with pip

If you'd like to download the source of your dependencies node-style, you can do something like that with pip:

```pip install foo --download=some/path --no-binary :all:```

`--download` specifies where you want to put the dependency's source. `--no-binary :all:` indicates that you don't want to download wheel files for any of these dependencies.

You'll end up with a bunch of .tar.gz files in `some/path`.

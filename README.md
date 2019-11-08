This repository covers the following recipe from code.activestate.com:

[DIRT SIMPLE MAP/REDUCE
](https://code.activestate.com/recipes/577676/)

*Created by Raymond Hettinger on Mon, 25 Apr 2011*

Simple tool for analyzing datasets.

Provides minimal pivot-table and crosstab capabilities.

The recipe can also be implemented using collections.defaultdict(). The current implementation was chosen for clarity and to simplify the signature (user's expect map/reduce to return a regular dict). Another goal was to use dirt simple Python for the map_reduce() function.

The recipe uses math.fsum() instead of the builtin sum() to make sure precision isn't lost when averaging a large dataset full of nearly equal values.

Named tuples are used for code clarity but aren't essential to the map_reduce() recipe.

## Usage

If you already have the [State Tool] installed you can simply run

```
state activate ActiveState-Recipes/recipe-577676-dirt-simple-mapreduce
```

If you do not have the [State Tool] installed you can use the following convenient one-liner.

Linux: 
```
sh <(curl -q https://platform.activestate.com/dl/cli/install.sh) -n -f && state activate --path $HOME/ActiveState-Recipes/recipe-577676-dirt-simple-mapreduce ActiveState-Recipes/recipe-577676-dirt-simple-mapreduce
```

Windows: 
```
powershell "Set-Item -Path Env:NOPROMPT_INSTALL -Value 'true'; IEX(New-Object Net.WebClient).downloadString('https://platform.activestate.com/dl/cli/install.ps1')" && state activate --path %APPDATA%/ActiveState-Recipes/recipe-577676-dirt-simple-mapreduce ActiveState-Recipes/recipe-577676-dirt-simple-mapreduce
```

macOS: not yet supported

[State Tool]: https://www.activestate.com/products/platform/state-tool/
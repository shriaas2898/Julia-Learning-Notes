
### 1. Installing IJulia with existingnbextensions plotly com jupyter notebook.
Setting path of `jupyter` after installing through Pkg.add.
    
**Description:** I accidentaly set wrong path of jupyter to `ENV["JUPYTER"]` variable before installing IJulia through Pkg.add
I even tried changing path and doing Pkg.build("IJulia") which didn't worked
      
**Solution:** After changing path and calling build just restart `julia` and it then open `notebook()` it should work

### 2. Using plotlyjs with jupyter notebook:

**Description:** Using plotlyjs can be a little tricky you have to install certain things in order to make it work.
    
**Solution:** 1. Install and build ORCA:
```julia
using Pkg
Pkg.add("ORCA")
Pkg.build("ORCA")
```
2. Install and build WebIO:
```julia
Pkg.add("WebIO")
Pkg.build("WebIO")
```
3. Install plotlyjs
```julia
Pkg.add("plotlyjs")
```
4. Add plotly extension to jupyter notebook:
* [Using conda](https://anaconda.org/conda-forge/jupyterlab-plotly-extension)
* [Using JupyterLab Extension Manager](https://jupyterlab.readthedocs.io/en/stable/user/extensions.html)

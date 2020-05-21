**Date:** 16th May 2020
1. Installing IJulia with existing jupyter notebook 
    1.1Setting path of `jupyter` after installing through Pkg.add
    **Description:** I accidentaly set wrong path of jupyter to `ENV["JUPYTER"]` variable before installing IJulia through Pkg.add
      I even tried changing path and doing Pkg.build("IJulia") which didn't worked
      
    **Solution:** After changing path and calling build just restart `julia` and it then open `notebook()` it should work

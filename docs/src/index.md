```@meta
DocTestSetup = quote
    using ColorSchemes, Colors
end
```

# Introduction to ColorSchemes
This package provides a collection of colorschemes:

- scientifically devised colorschemes from ColorBrewer, CMOcean, ScientificColorMaps, ColorCet, and Seaborn
- popular old favourites such as _viridis_, _inferno_, and _magma_ from MATPlotLib
- old masters' colorschemes, such as _leonardo_, _vermeer_, and _picasso_
- variously themed colorschemes such as _sunset_, _coffee_, _neon_, and _pearl_

Note that the schemes contained here are a mixture:

- some are high quality color maps with consistent perceptual contrast over their full range
- others are designed for general purpose and informal graphics work

Choose colorschemes with care! Refer to Peter Kovesi's [PerceptualColourMaps](https://github.com/peterkovesi/PerceptualColourMaps.jl) package, or to Fabio Crameri's [Scientific Colour Maps](http://www.fabiocrameri.ch/colourmaps.php) for more information.

This package relies on the [Colors.jl](https://github.com/JuliaGraphics/Colors.jl) package.

If you want to make more advanced ColorSchemes, use linear-segment dictionaries or indexed lists, and use functions to generate color values, see the `make_colorscheme()` function in the [ColorSchemeTools.jl](https://github.com/JuliaGraphics/ColorSchemeTools.jl) package.

## Installation and basic usage

Install the package as follows:

```julia
import Pkg
Pkg.add("ColorSchemes")
```

or, at the REPL:

```julia
] add ColorSchemes
```

Usage:

```julia
using ColorSchemes

ColorSchemes.Purples_5 
# => a ColorScheme 

colorschemes[:Purples_5]
# => a ColorScheme 

ColorSchemes.Purples_5.colors
# => array of five RGB colors

ColorSchemes.Purples_5.colors[3]
# => the third color in the colorscheme

get(ColorSchemes.Purples_5, 0.5)
# => the midway point of the colorscheme 

colorschemes
# => Dict{Symbol, ColorScheme} with 983 entries

findcolorscheme("purple")
# => display list of matching schemes
```

Original version by [cormullion](https://github.com/cormullion).

## Documentation

This documentation was built using [Documenter.jl](https://github.com/JuliaDocs).

```@example
using Dates # hide
println("Documentation built $(Dates.now()) with Julia $(VERSION)") # hide
```

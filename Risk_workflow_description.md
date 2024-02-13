# My workflow  

This template workflow should help us make sure that all the notebooks have the same structure.  
The green 'tip' boxes are there with the example text. **Make sure you delete them when you add your own text**.  
Replace 'tip' with 'note', 'hint', 'warning', 'info', 'caution' to get other colours.  See other [admonition types in Myst Markdown documentation](https://myst-parser.readthedocs.io/en/latest/syntax/admonitions.html).

Useful links:

- [Jupyter book documentation](https://jupyterbook.org/en/stable/intro.html)
- [MyST Markdown documentation](https://myst-parser.readthedocs.io/en/latest/index.html)

## Risk assessment methodology

Write here a description of the methodology.  

Describe the workflow and the data that is used.

In particular, start with a brief description of the type of hazard and sector (e.g. building environment, agriculture, etc) for your given risk workflow (e.g. heatwave). Use max 250 words.
Then, include a description of the type of approach used for risk calculation (e.g. damage analysis, risk matrix, or vulnerability/exposure calculation). Use max 500 words.
This will help the reader understand how risk is calculated.

Describe where the data can be found, is there an API to download it or the files can be downloaded from some data repository? Provide a link to the repository (as DOI if possible).

````{admonition} This is the example of the text description of the data in a green box:
:class: seealso

- River flood extent and water depth: available from the [JRC repository](https://data.jrc.ec.europa.eu/dataset/1d128b6c-a4ee-4858-9e34-6210707f3c81) for different return periods. Flood extent map of 100m resolution
- Land-use information: The land cover map and all the spatial projections of population and land cover are available from the [JRC Data Catalogue](https://data.jrc.ec.europa.eu/collection/luisa)
- Flood damage: assessed as a combination between flood extent/water depths and damage curve (available [here](https://publications.jrc.ec.europa.eu/repository/handle/JRC105688). For each pixel, the water depths are used as input in the damage curve to assess the damage, together with different land use and country.
- Flood affected population is assessed by overlaying the [European population density map at 100 m resolution](https://doi.org/10.6084/m9.figshare.6210392) with the flood inundation maps for a given return map. Another possible dataset is the [Global Human Settlement Population dataset](https://ghsl.jrc.ec.europa.eu/download.php?ds=pop) which also has 100m resolution as the JRC flood data.
````

And some example of text:  
**Probabilistic assessment of flood damage** is calculated for different return periods (i.e. 2, 5, 10, 20, 50, 100, 250 and 500 years). In this way, damage-probability curves can be obtained at the grid cell by interpolating the damage estimates between the different recurrence intervals considered. The expected annual damages at a given grid cell due to river flooding are thus the integral of the damage-probability curve. Flood protection can be included in the expected annual damages estimation by truncating the damage-probability curves at the corresponding protection level (e.g. design flood with return period of 100 years). The integral of the remaining part after truncation quantifies the expected annual damages and expected annual population affected caused by river flooding considering flood protection up to the design flood.  
Similar to flood damages, population exposure probability functions can be derived for each grid cell within the modelled domain.  

Example of adding an image  
```{figure} images/Heavy-flooding-in-a-town-scaled.webp
---
name: Name of my image
height: 400px
align: center
---
Text that goes below + [licence source](https://www.rawpixel.com/image/5914270/image-public-domain-houses-water)
```


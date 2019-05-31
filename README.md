### Installation
The PyBEM module requires the following anciliary software, packages, and libraries:
  - [Python 2.7](https://www.python.org/downloads/release/python-2713/) or [above](https://www.python.org/downloads/release/python-373/) - a modern programming language
  - [EnergyPlus 8.9.0](https://github.com/NREL/EnergyPlus/releases/tag/v8.9.0) - a whole building energy simulation software
  - [eppy](https://eppy.readthedocs.io/en/latest/installation.html) - a python-based programming language for EnergyPlus input and output files
  - [numpy](https://www.numpy.org/)- a package for scientific computing with Python 
  - [pandas](https://pandas.pydata.org/) - a Python package for data analysis 
  - [matplotlib](https://matplotlib.org/users/installing.html) - a Python 2D data visualization library

### PyBEM - What is it?
  Ipsum Dolor sit amet ...

### Using PyBEM - A quick tutorial
<details> 
  <summary> <b> Creating a building (energy model) </b> </summary>
  
  First of all we need to import the PyBEM module which includes several auxiliary functions and the BEM class with its attributes and methods.
  
  {% highlight python %}
  from PyBEM import pybem
  from PyBEM.pybem import *
  {% endhighlight %}
  
  Then we call the 'BEM' class to instantiate an building energy model (BEM). To instantiate the class we need to provide (in order): 
  1. Number of floors
  2. Width
  3. Length
  4. Floor Height - by default is set to 3 m
  5. Window-to-Wall Ratio (WWR) - by default is set to 40 (%)
  6. Location - i.e., the path to an EnergyPlus weather file (epw) - a text file that contains Typical Metereological Year data of a specific location. By default, the location is set to Phoenix, AZ. [EnergyPlus website](https://energyplus.net/weather) provides an extensive library of epw files for diferent locations around the globe.
  7. Rotation - by default is set to 0&deg;. PyBEM only supports a rotation angle from 0&deg; to 90&deg; 
  
  Below is an example of how to create a BEM of a 60 by 30 m building with 5 floors with PyBEM. The floor height, location, WWR, and rotation values are the default ones.
  
  {% highlight python %}
  bldg01 = BEM(5, 60, 30)
  {% highlight python %}
  
  The following generates a building of 25 by 70 m building with 15 floors, each one with a floor to ceiling height of 3 m, with a rotation angle of 30&deg;. The location and WWR values are the default ones.
 
  {% highlight python %}
  bldg02 = BEM(15, 25, 70, rotation= 30.0)
  {% highlight python %}
  
</details>

<details> 
  <summary> <b> Changing the rotation of the model </b> </summary>
  After instantiating an energy model by using the BEM class, PyBEM allows to change several object properties such as the rotation of the building. PyBEM only allows to rotate the building model in a continuous range from 0&deg; to 90&deg;. However, due to the rectangular plan shape of the models produced by PyBEM, this ranges allows the simulation of any possible exposure scheme of a shoe box energy model. By default the rotation angle is 0&deg;. Because the original facades can assume different exposures/orientations, PyBEM labels each facade as shown in Figure 1 (below):
  
  - to do - insert Figure 1
  
  To change the rotation (and consequently the orientation) of an already instantiated model, we should use the _changeRotation_ method in the object. This method receives a rotation angles in degrees (float or integer). Below is an example to rotate the instance **bldg01** generated in the previous section.
  
  {% highlight python %}
  bldg01.changeRotation(45)
  {% endhighlight %}
  
</details>


<details> 
  <summary> <b> Changing Window-to-Wall (WWR) ratio </b> </summary>
  
  Content coming soon.
</details>

<details> 
  <summary> <b> Changing building envelope properties </b> </summary>
  
  Content coming soon.
</details>

<details> 
  <summary> <b> Visualizing the Model </b> </summary>
  
  Content coming soon.
</details>


<details> 
  <summary> <b> Simulating a Building </b> </summary>
  
  Content coming soon.
  
</details>

### 

### PyBEM - Class atributes and methods
<details> 
  <summary> <b> Atributes </b> </summary>
  
  Content coming soon.
</details>

<details> 
  <summary> <b> Methods </b> </summary>
  
  Content coming soon.
</details>

# MARKDOWN TEMPLATE GUIDE (to be deleted)
## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/luissds82/buildingenergymodeler.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3
#### Header 4

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/luissds82/buildingenergymodeler.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

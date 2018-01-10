# Telematic Exploratory Data Analysis

My research was centred on sensing systems, I am always fascinated when it comes to making sense out of or figuring patterns from sensing data. 
In this post, I am going to explore sensing data in cars. The goal here is to find insights from this sensing data and possibly develop usecases and value propositions of the importance of having sensors installed in cars, whether for personal use or businesses.  

Luckily, I laid hold on a telematic dataset from United Arab Emirate. The  dataset contains information about 10 cars driving on October 8, 2016. A very important point first. October 8, 2016 is Saturday, which is a weekend in United Arab Emirates (cars coordinates are in this country), so this influences the people activity: some could work, some could entertain themselves, some could buy products for the week and so on.

Also some additional information:
As far as I know speed limit in United Arab Emirates is up to 120 km/h on main roads and 140 km/h on some major express highways(Boy, that's some car racing speed right there). Many drivers maintain higher speed between the speed cameras. So drivers with speeds exceeding the limits should be considered risky.

My analysis goes through the following steps:

- data preparation (dropping unnecessary data and duplicate rows as well as transforming variables);
- looking at basic general information about the cars;
- main analysis of the data and drawing driving pathes of the cars;
- conclusions;


## Software requirements

This post is based on **Python 3**. I cannot guarantee that the materials will work well with Python 2 or earlier, so ensure Python 3.5 or greater is installed on your system.

I recommend installing the [Anaconda](https://www.continuum.io/downloads) distribution of Python 3, as it allows for the easy automation of package installation and virtual environment creation (see instructions below).

## Getting the materials

Clone this repository into a directory of your choice.

    git clone https://github.com/udohsolomon/telemetry.git

If you are not familiar with Git and GitHub, you can simply download the zip file of the repository at the top of the main repository page.

Then, move to the directory created by the clone/zip file:

    cd telemetry

and install everything using `conda`:

    conda env create -f environment.yml

This will create an **environment** called `telemetry` that includes the packages required for the course.    

If you are not using the Anaconda Python distribution, you will need to manually install the packages listed in `environment.yml` using `pip`.

Which you probably don't want to do.

So [install Anaconda](https://www.continuum.io/downloads).

To use the environment, you may type:

    source activate telemetry

# Ladybug Tools Grasshopper Plugin Installation

Below are the instructions to install the Ladybug Tools Grasshopper Plugin.
Following them will allow you to get a fully-working version of the Ladybug Tools
Plugin for free, which is possible because all of Ladybug Tools and the engines
it uses are [open source](https://en.wikipedia.org/wiki/Open_source).

If you are looking for a faster installation with fewer steps, Ladybug Tools also
sells a single-click executable installer, which is recommended when installing
on computers managed by an IT department.

However, if you are on your own machine and you enjoy learning about what is
under the hood of your software, you have come to the right place!

## Installation Steps

The steps below work on both Windows and Mac, though you will see the exact location of
the installation will vary slightly.

1. Download the latest version of [Ladybug Tools from Food4Rhino](https://www.food4rhino.com/app/ladybug-tools).

2. Inside the download, you will find an installer.gh file. Open it in Grasshopper
and you should see something similar to the following:
![installer.gh File](https://user-images.githubusercontent.com/5567574/84212420-c1fd4b00-aa8b-11ea-8928-5384f0e9c9eb.png)
Set the first toggle to True.

3. The component will tell you that you need to install 3 other software packages,
the first of which is Python.
![Run First Component](https://user-images.githubusercontent.com/5567574/84212936-3edcf480-aa8d-11ea-9dfd-322db69be799.png)
Python is the computer language in which Ladybug Tools is written and is one of
the fastest-growing programming languages.
[Download the latest version of Python from python.org](https://www.python.org/downloads/)

4. Run the Python executable and select "Custom Installation"
![Python custom Installation](https://user-images.githubusercontent.com/5567574/84213232-21f4f100-aa8e-11ea-90b3-1cd7f92bac86.png)
When you get to "Advanced Options," __BE SURE TO INSTALL IT IN THE FOLDER NOTED IN THE INSTALLER.GH__ like so:
![Install Python Location](https://user-images.githubusercontent.com/5567574/84213410-916ae080-aa8e-11ea-8190-15865a038430.png)

5. The second software package you need to install is OpenStudio. OpenStudio is a
programming interface for EnergyPlus, which is the engine that Honeybee uses for
building energy simulation. Check the compatibility matrix below to determine which
version of OpenStudio is compatible with your version of Ladybug Tools.
[Download that version of OpenStudio from the OpenStudio Github](https://github.com/NREL/OpenStudio/releases)

6. Run the OpenStudio executable. When you get to "Installation Folder,"
__BE SURE TO INSTALL IT IN THE FOLDER NOTED IN THE INSTALLER.GH__ like so:
![Install OpenStudio Location](https://user-images.githubusercontent.com/5567574/84213878-cf1c3900-aa8f-11ea-8ac6-6316e16df98e.png)

7. The second software package you need to install is Radiance. Radiance is a physics-based
rendering engine, which is what Honeybee uses for all daylight and spatial solar studies.
Check the compatibility matrix below to determine which version of Radiance is
compatible with your version of Ladybug Tools.
[Download that version of Radiance from the Radiance Github](https://github.com/NREL/Radiance/releases)

8. Run the Radiance executable. When you get to "Installation Folder,"
__BE SURE TO INSTALL IT IN THE FOLDER NOTED IN THE INSTALLER.GH__ like so:
![Install Radiance Location](https://user-images.githubusercontent.com/5567574/84214321-0b03ce00-aa91-11ea-943a-ba109694dfe0.png)

9. Finally, go back to the installer.gh file and set the second toggle to true:
![Run Second Component](https://user-images.githubusercontent.com/5567574/84214364-2a9af680-aa91-11ea-8ba5-65c6041fbea6.png)
It will take a few seconds to download the correct versions of Ladybug Tools.

10. If the component runs to completion without turning red, congratulations! You did
the steps correctly and you now have a working version of Ladybug Tools.

## Compatibility Matrix

This matrix records which version of Ladybug Tools is compatible with each
language/simulation engine.

| Ladybug Tools | Python | OpenStudio | Radiance |
| ------------- | ------ | ---------- | -------- |
| 1.0.0         | >=3.6  | 3.0.0      | 5.3      |

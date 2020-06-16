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

1. Download the latest version of [Ladybug Tools from Food4Rhino](https://www.food4rhino.com/app/ladybug-tools).

2. Inside the download, you will find an installer.gh file. Open it in Grasshopper
and set the first toggle to True. The component will tell you that you need to
install 3 other software packages, the first of which is Python.

![Run First Component](https://user-images.githubusercontent.com/5567574/84212936-3edcf480-aa8d-11ea-9dfd-322db69be799.png)

3. Python is the computer language in which Ladybug Tools is written and is one of
the fastest-growing programming languages. Ladybug Tools uses a special build of
Python that can be [downloaded from this link as a .zip file](https://ladybug-tools-releases.nyc3.digitaloceanspaces.com/python_3.82_windows.zip).

4. Download the file and, before you unzip it, right-click it and select "Properties".
Check the "Unblock" bok and then hit "OK."

![Unblock Zip File](https://user-images.githubusercontent.com/5567574/84812685-c4f0c200-afdc-11ea-9328-aa2dccdb656b.png)

5. Unzip the file __INTO THE FOLDER NOTED IN THE INSTALLER.GH__. This should
be `C:\Users\[USERNAME]\ladybug_tools\python` but with your own username for `[USERNAME]`.
At the end you should have something that looks like this:

![Install Python Location](https://user-images.githubusercontent.com/5567574/84322480-11528280-ab43-11ea-82dd-3b19af31d7b0.png)

6. The second software package you need to install is OpenStudio. OpenStudio is a
programming interface for EnergyPlus, which is the engine that Honeybee uses for
building energy simulation. Check the compatibility matrix below to determine which
version of OpenStudio is compatible with your version of Ladybug Tools.
[Download that version of OpenStudio from the OpenStudio Github](https://github.com/NREL/OpenStudio/releases)

7. Run the OpenStudio executable. When you get to "Installation Folder,"
__INSTALL IT IN THE FOLDER NOTED IN THE INSTALLER.GH__. Note that you should use
your own username for `[USERNAME]`.

![Install OpenStudio Location](https://user-images.githubusercontent.com/5567574/84213878-cf1c3900-aa8f-11ea-8ac6-6316e16df98e.png)

8. The third software package you need to install is Radiance. Radiance is a physics-based
rendering engine, which is what Honeybee uses for all daylight and spatial solar studies.
Check the compatibility matrix below to determine which version of Radiance is
compatible with your version of Ladybug Tools.
[Download that version of Radiance from the Radiance Github](https://github.com/LBNL-ETA/Radiance/releases)

9. Run the Radiance executable. When you get to "Choose Install Location,"
__INSTALL IT IN THE FOLDER NOTED IN THE INSTALLER.GH__. Note that you should use
your own username for `[USERNAME]`.

![Install Radiance Location](https://user-images.githubusercontent.com/5567574/84214321-0b03ce00-aa91-11ea-943a-ba109694dfe0.png)

10. Go back to the installer.gh file and set the second toggle to true:

![Run Second Component](https://user-images.githubusercontent.com/5567574/84214364-2a9af680-aa91-11ea-8ba5-65c6041fbea6.png)
It will take a few seconds to download the Ladybug Tools core libraries into the
Python installation that you unzipped earlier. This component also downloads all
of the Ladybug Tools Grasshopper components. Lastly, a library of default assets
(Energy Constructions, Radiance Modifiers, etc.) will be downloaded to
`\ladybug_tools\resources\standards`.

11. You are almost there but there's one more step! If the component runs to
completion without turning red, you did the previous steps correctly. Now there's
just one last step that must be run __WITH RHINO CLOSED__. Close Rhino and you will
see that there is a file named `set_python_path.bat` in your ladybug_tools folder:

![set_python_path.bat](https://user-images.githubusercontent.com/5567574/84816165-13ed2600-afe2-11ea-855c-c259c66f9b3b.png)

Double-click it and this will set Rhino to look for the Ladybug Tools core libraries
in the `ladybug_tools\python` folder.


12. Open Rhino and you should see the Ladybug Tools components available in new tabs.
Congratulations! You now have a working version of Ladybug Tools.

## Compatibility Matrix

This matrix records which version of Ladybug Tools is compatible with each
language/simulation engine.

| Ladybug Tools | Python | OpenStudio | Radiance       |
| ------------- | ------ | ---------- | -------------- |
| 1.0.0         | 3.82   | 3.0.0      | 5.2.e4d2f765dc |

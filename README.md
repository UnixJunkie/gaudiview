# GaudiView #

Light interface to explore solutions from GAUDIasm and others, inside UCSF Chimera

## Usage

1. Open up Chimera and launch `GAUDI> GaudiView`.
2. Select a YAML-formatted `*.gaudi` file, as generated by GAUDI. It will also display GOLD results if you choose the corresponding `gold.conf` file.
3. Click on the solutions you want to view. `Ctrl` and `shift` click will handle multiple selections. You can also navigate with up and down arrows.
4. The list can be multisorted and filtered. Feel free to experiment.
5. Double-click updates rotamers and mutamers in the protein, if available.
6. If you want to perform some actions on every pose, write a Chimera command and it will be executed every time the selection changes.

## Requirements

**Dependencies**

* **[UCSF Chimera](http://www.cgl.ucsf.edu/chimera/download.html)**. Main framework.

* **[PyYaml](https://pypi.python.org/pypi/PyYAML) package**. GAUDIasm file parsing.

* **[tkintertable](https://pypi.python.org/pypi/tkintertable) package**. Sortable and filterable table.


## Installation
1 - Download the [latest stable copy](http://www.cgl.ucsf.edu/chimera/download.html) and install it with:

    chmod +x chimera-*.bin && ./chimera-*.bin


2 - Locate the installation directory. The default location is `~/.local/UCSF-Chimera<arch>-<version>`, so adapt it for your version. For example, the binary of a 64-bit Chimera v1.10.1 will be at `~/.local/UCSF-Chimera64-1.10.1`. 

3 - Download the latest copy of **GaudiView** or `git clone` the repository, and place it inside `~/.local/UCSF-Chimera<arch>-<version>/share/` (adapt it to your version). You can also `ln -s` to any other location.

4 - Download [tkintertable](https://pypi.python.org/pypi/tkintertable) source package and extract the `*tar.gz` file. Open Chimera display and click on `Favorites> Command Line`. This will bring an input field to the GUI, in which you need to type the following commands. Press `Enter` after each line.

	cd /path/to/where/tkintertable/was/extracted/
	runscript setup.py install

5 - Repeat step 4 with [PyYaml](https://pypi.python.org/pypi/PyYAML) source package. Et voilà!

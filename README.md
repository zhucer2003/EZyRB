<p align="center">
  <a href="http://github.com/mathLab/PyDMD/" target="_blank" >
    <img alt="Python Dynamic Mode Decomposition" src="readme/logo_EZyRB_small.png" width="200" />
  </a>
</p>
<p align="center">
    <a href="https://github.com/mathLab/EZyRB/blob/master/LICENSE.rst" target="_blank">
        <img alt="Software License" src="https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square">
    </a>
    <a href="https://travis-ci.org/mathLab/EZyRB" target="_blank">
        <img alt="Build Status" src="https://travis-ci.org/mathLab/EZyRB.svg">
    </a>
    <a href="https://coveralls.io/github/mathLab/EZyRB" target="_blank">
        <img alt="Coverage Status" src="https://coveralls.io/repos/github/mathLab/EZyRB/badge.svg">
    </a>
    <a class="badge-align" href="https://www.codacy.com/app/mathLab/EZyRB?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=mathLab/EZyRB&amp;utm_campaign=Badge_Grade">
        <img src="https://api.codacy.com/project/badge/Grade/045ccb10d2ff470f98f8e2baac8bd5cd"/>
    </a>
</p>


**EZyRB**: Easy Reduced Basis method

## Table of contents
* [Description](#description)
* [GUI](#graphical-user-interface)
* [Dependencies and installation](#dependencies-and-installation)
* [Documentation](#documentation)
* [Testing](#testing)
* [Examples](#examples)
* [How to cite](#how-to-cite)
	* [Recent works with EZyRB](#recent-works-with-ezyrb)
* [Authors and contributors](#authors-and-contributors)
* [How to contribute](#how-to-contribute)
	* [Submitting a patch](#submitting-a-patch) 
* [License](#license)

## Description
**EZyRB** is a python library for the Model Order Reduction based on **baricentric triangulation** for the selection of the parameter points and on **Proper Orthogonal Decomposition** for the selection of the modes. It is ideally suited for actual industrial problems, since its structure can interact with several simulation software simply providing the output file of the simulations. Up to now, it handles files in the vtk and mat formats. It has been used for the model order reduction of problems solved with matlab and openFOAM.

See the [**Examples**](#examples) section below and the **Tutorials** to have an idea of the potential of this package.

## Graphical User Interface
**EZyRB** is now provided with a very basic Graphical User Interface (GUI) that, in Ubuntu environment, looks like the one depicted below. This feature can be easily used even by the pythonists beginners with not much effort. Just see the [tutorial 4](https://github.com/mathLab/EZyRB/blob/master/tutorials/tutorial-4-gui.ipynb). For the laziest, also a [video tutorial on YouTube](https://youtu.be/PPlRHu53VRA) is available.

<p align="center">
<img src="readme/EZyRB_gui.png" alt>
</p>
<p align="center">
<em>EZyRB GUI: how it appears when it pops up.</em>
</p>

Up to now, EZyRB GUI works on linux and Mac OS X computers.

## Dependencies and installation
**EZyRB** requires `numpy`, `scipy` and `matplotlib`. They can be easily installed via `pip`. Moreover **EZyRB** depends on `vtk`. These requirements cannot be satisfied through `pip`.
Please see the table below for instructions on how to satisfy the requirements.

| Package | Version  | Comment                                                                    |
|---------|----------|----------------------------------------------------------------------------|
| vtk     | >= 5.0   | Simplest solution is `conda install vtk`                                   |

The official distribution is on GitHub, and you can clone the repository using

```bash
> git clone https://github.com/mathLab/EZyRB
```

To install the package just type:

```bash
> python setup.py install
```

To uninstall the package you have to rerun the installation and record the installed files in order to remove them:

```bash
> python setup.py install --record installed_files.txt
> cat installed_files.txt | xargs rm -rf
```


## Documentation
**EZyRB** uses [Sphinx](http://www.sphinx-doc.org/en/stable/) for code documentation. To build the html versions of the docs simply:

```bash
> cd docs
> make html
```

The generated html can be found in `docs/build/html`. Open up the `index.html` you find there to browse.


## Testing
We are using Travis CI for continuous intergration testing. You can check out the current status [here](https://travis-ci.org/mathLab/EZyRB).

To run tests locally:

```bash
> python test.py
```



## Examples

You can find useful tutorials on how to use the package in the `tutorials` folder.
Here we show an applications taken from the **automotive** engineering fields

<p align="center">
<img src="readme/pod_modes.png" alt>
</p>
<p align="center">
<em>The first POD modes of the pressure field on the DrivAer model.</em>
</p>

<p align="center">
<img src="readme/errors.png" alt>
</p>
<p align="center">
<em>DrivAer model online evaluation: pressure (left) and wall shear stress (right) fields and errors.</em>
</p>


## How to cite
If you use this package in your publications please cite the package as follows:

```tex
\bibitem{ezyrb}
{EZyRB: Easy Reduced Basis method. Available at}: \href{https://github.com/mathLab/EZyRB}{https://github.com/mathLab/EZyRB}.
```

### Recent works with EZyRB
Here there is a list of the scientific works involving **EZyRB** you can consult and/or cite. If you want to add one, please open a PR.


## Authors and contributors
**EZyRB** is currently developed and mantained at [SISSA mathLab](http://mathlab.sissa.it/) by
* [Nicola Demo](mailto:demo.nicola@gmail.com)
* * [Marco Tezzele](mailto:marcotez@gmail.com)

under the supervision of [Prof. Gianluigi Rozza](mailto:gianluigi.rozza@sissa.it). We thank [Filippo Salmoiraghi](mailto:filippo.salmoiraghi@gmail.com) for the original idea behind this package and the major contributions.

Contact us by email for further information or questions about **EZyRB**, or suggest pull requests. **EZyRB** is at an early development stage, so contributions improving either the code or the documentation are welcome!


## How to contribute
We'd love to accept your patches and contributions to this project. There are
just a few small guidelines you need to follow.

### Submitting a patch

  1. It's generally best to start by opening a new issue describing the bug or
     feature you're intending to fix.  Even if you think it's relatively minor,
     it's helpful to know what people are working on.  Mention in the initial
     issue that you are planning to work on that bug or feature so that it can
     be assigned to you.

  2. Follow the normal process of [forking][] the project, and setup a new
     branch to work in.  It's important that each group of changes be done in
     separate branches in order to ensure that a pull request only includes the
     commits related to that bug or feature.

  3. To ensure properly formatted code, please make sure to use 4
     spaces to indent the code. The easy way is to run on your bash the provided
     script: ./code_formatter.sh. You should also run [pylint][] over your code.
     It's not strictly necessary that your code be completely "lint-free",
     but this will help you find common style issues.

  4. Any significant changes should almost always be accompanied by tests.  The
     project already has good test coverage, so look at some of the existing
     tests if you're unsure how to go about it. We're using [coveralls][] that
     is an invaluable tools for seeing which parts of your code aren't being
     exercised by your tests.

  5. Do your best to have [well-formed commit messages][] for each change.
     This provides consistency throughout the project, and ensures that commit
     messages are able to be formatted properly by various git tools.

  6. Finally, push the commits to your fork and submit a [pull request][]. Please,
     remember to rebase properly in order to maintain a clean, linear git history.

[forking]: https://help.github.com/articles/fork-a-repo
[pylint]: https://www.pylint.org/
[coveralls]: https://coveralls.io
[well-formed commit messages]: http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
[pull request]: https://help.github.com/articles/creating-a-pull-request


## License

See the [LICENSE](LICENSE.rst) file for license rights and limitations (MIT).

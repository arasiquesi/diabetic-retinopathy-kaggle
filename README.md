Diabetic Rethinopathy (keggle competition)
==========================================

## Manifesto

Because *Human* is **perfectible** and **error-prone**, because *Science* should be **open** and **flow** and because *cogito ergo sum*.
Research project initialization and organization following reproducible research guidelines.

Project folder structure
------------------------

This project has been structured using this [rr-init repository] as a template.
In order to keep an upstream to such project, add it as remote like this:

```
git remote add rr-initUPS git@github.com:massich/rr-init.git
```

### Structure Description
```
    project
    |- doc/                  # documentation for the study
    |  |- literature_review/ # some of the working papers we are using
    |  +- paper/             # manuscript(s), whether generated or not
    |
    |- data                  # raw and primary data, are not changed once created
    |  |- raw/               # raw data, will not be altered
    |  +- clean/             # cleaned data, will not be altered once created
    |
    |- results               # all output from workflows and analyses
    |  |- figures/           # graphs, likely designated for manuscript figures
    |  +- pictures/          # diagrams, images, and other non-graph graphics
    |
    |- scratch/              # temporary files that can be safely deleted or lost
    |- src/                  # any programmatic code
    |
    |- Makefile              # executable Makefile for this study, if applicable
    |- datapackage.json      # metadata for the (input and output) data files
    |- requirements.txt      # list of the required packages (see virtualenv)
    |
    |- LICENSE.md
    |- README.md             # the top level description of content
```

### Recomendations

#### Use a virtual environment (Virtualenv + VirtualenvWrapper)

Virtual-environments are not **virtual machines**.
Virtual-environments are used to avoid library classing between the libraries of a project and those fom the system.
Find more information in this [virtual environment post] describing how to use virtual environment for a [mozilla marketplace testing].

Use the following to create a `diabetes` environment based on the `./requirements.txt` associated with the source directory `./src`:

```
mkvirtualenv diabetes -a src -r ../requirements.txt
```

Notice that `mkvirtualenv` activates such environment.
The command `deactivate` is used to exit the virtual environment.
Once the virtual environment exist on the system, the command `workon diabetes` is rather convenient since it jumps into the working directory and activates the virtual enviroment.

**Remember** to keep `requirements.txt` up to date.
For more details regarding the usage of the virtual enviroment, please look at the [command reference].

Similar Projects
----------------

- [check project A]
- [check project B]
- [check project C]
- [check project D]
- [check project E]
- [check project F]

Todo
----

- [ ] Add virtual-env behaviour (at /src)
- [ ] Add sphinx documentation as project.io website
- [ ] report how to download the data
- [ ] Data load example


[rr-init repository]: https://github.com/massich/rr-init

[virtual environment post]: http://www.silverwareconsulting.com/index.cfm/2012/7/24/Getting-Started-with-virtualenv-and-virtualenvwrapper-in-Python
[mozilla marketplace testing]: https://github.com/mozilla/marketplace-tests
[command reference]:http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html

[check project A]: https://github.com/manasidesh2311/DiabeticRetinopathy
[check project B]: https://github.com/lantian2012/CS205_Project
[check project C]: https://github.com/vamshins/ML-Kaggle-Diabetic-Retinopathy/tree/master/DiabeticRetinopathy
[check project D]: https://github.com/ebenolson/kaggle-drc-viewer
[check project E]: https://github.com/domspad/kaggleDiabetes
[check project F]: https://github.com/deworrall92/ROP/tree/master/dev

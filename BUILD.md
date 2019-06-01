# Creating a Local Development Environment

Use the following script to create a python virtual environment and install
the required dependencies 

    ./create_local_env.sh

# Local build

Before pushing commits you should locally build to run tests, check formatting
and documentation. Use the following command to run the build

    ./pre_push.sh

# Continuous Integration - Travis

CI is performed on Travis. The configuration file is

    .travis.yml
    
A slight modification needed to be made to the normal Travis config in order
for Python 3.7 to work
https://github.com/travis-ci/travis-ci/issues/9069#issuecomment-425720905

# PEP8 Formatting

To check PEP8 formatting we use flake8. Run flake8 by using the following
command, which will automatically discover the configuration in ``setup.cfg``

    flake8
    
To automatically format our code to PEP8 standard we use black. Run black by
using the following command which will automatically discover the configuration
in ``pyproject.toml``

    black ./    

black will not reformat comments, so it is important that you run flake8
locally to discover any issues before pushing.
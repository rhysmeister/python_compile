# python_compile
Compile various Python versions from source on Debian

# Default variables

python_version: String - should be a value from https://www.python.org/ftp/python/
python_src_url: Python source download url, built using python_version.
python_root_parent: Parent directory where Python sources will be placed. Default "/opt"
python_root: Roto directory for python sources.
pre_build_packages: List of packages required for various tasks.
build_packages: Package required for the build.
build_threads: Number of build threads. Default 4.
make_install_method: Make install command, default altinstall


||OS||Default Python||
|Debian Bullseye|Python 3.9|
|Debian Buster|Python 3.7 & 2.7|
|Debian Stretch|Python 3.5 & 2.7|

# Run Molecule tests

* Create a Python Virtual Environment

```bash
virtualenv venv
```

* Source the venv

```bash
source venv/bin/activate
```

* Install the requirements

```bash
pip install -r requirements.txt
```

* Run the tests

```bash
molecule test
```
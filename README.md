# **PyPi Package Links**
#### **Here ae my Python packages available on PyPi:**

- PyPi link for awaish-pkg : [click here](https://pypi.org/project/awaish-pkg/)
- PyPi link for abu-project : [click here](https://pypi.org/project/abu-project/)
- pypi link for pattern-sort-package : [click here](https://pypi.org/project/pattern-sort-package/)
- pypi link for MysqlWebApp : [click here](https://pypi.org/project/MysqlWebApp/)

# Creating and Installing Python Wheel Packages

## **What is a Wheel File?**

A **Wheel** file is a binary package distribution format for Python, with the `.whl` extension. It contains all necessary files and metadata to make package installations faster and more efficient. Wheel files are optimized for faster installation and better dependency management when used with `pip`.

To install a wheel file, use the following command in the terminal:

```bash
pip install your_wheel_file_name.whl
```
**Make sure to open the terminal or command prompt in the same folder where your wheel file exists, or you can provide the full path to the wheel file.**

# **Steps to Create a Wheel File**
### Follow these steps to create your own Python wheel file:

#### **1. Create the Folder Structure**
**Create a new folder (let's call it project_folder) to hold your package.**
```bash
mkdir project_folder/
```

#### **2. Create Required Files in the Folder**
**Inside project_folder, create the following files:**

- **readme.txt**: Contains the package description or information.
- **LICENSE.txt**: License information for your package.
- **setup.py**: A script that contains the setup information for your package. It will look like this:
```bash
from setuptools import setup

setup(
    name="your_package_name",           # Name of your package
    version="0.1",                      # Version number
    description="A brief description of your package",  # Short description
    author="Your Name",                 # Author's name
    author_email="youremail@example.com",  # Author's email
    packages=["your_package"],          # List of all packages to include
    install_requires=["required_package_1", "required_package_2"],  # Dependencies
    # Add other setup arguments as needed
)
```
**In this file, you can customize the metadata and dependencies for your package.**

#### **3. Create Another Folder for Your Package Code**
**Inside project_folder, create another folder (let's call it your_package) where the Python code will reside**
```bash
project_folder/
    your_package/
        __init__.py  # This file contains the code for your package
```
**`The __init__.py` file is essential because it makes Python treat this folder as a package.**

#### **4. Build the Wheel File**
**Now, navigate to the project_folder and open your terminal or command prompt.**

**Run the following command to generate both the source distribution and the wheel file**
```bash
python setup.py sdist bdist_wheel
```
**This will create a `dist/` folder inside `project_folder/`, which will contain your `.whl file`.**

#### **5. Locate the Wheel File**
**After running the above command, navigate to the `dist/` folder:**
```bash
project_folder/
    dist/
        your_package_name-0.1-py3-none-any.whl  # This is the wheel file
```

#### **6. Install the Wheel File**
**To install your wheel file, use the following command**
```bash
pip install path_to_your_wheel_file/your_package_name-0.1-py3-none-any.whl
```
**Replace `path_to_your_wheel_file` with the actual path to your `.whl file`.**

# **How to Use the Installed Package**
**Once the wheel file is installed, you can use it in your Python project by importing it:**
```bash
import your_package
```
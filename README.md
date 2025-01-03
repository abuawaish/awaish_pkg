# awaish_pkg

`awaish_pkg` is a Python package designed to simplify the creation, distribution, and installation of Python libraries. It demonstrates the steps required to build a Python package and distribute it as a wheel file.

---

## PyPI Links

- **awaish_pkg**: [Click here](https://pypi.org/project/awaish-pkg/)
- **abu_project**: [Click here](https://pypi.org/project/abu-project/)
- **pattern_sort_package**: [Click here](https://pypi.org/project/pattern-sort-package/)

---

## What is a Wheel File?

A wheel file (`.whl`) is a binary distribution format in Python. It includes all the necessary files and metadata for a package, offering faster installation and better dependency management via `pip`.

---

## Installation  
### Ensure you are in the same folder as the wheel file, or provide its full path.  
 - To install a wheel file, use the following command in the terminal:

   ```bash
   pip install your_wheel_file_name.whl
   ```

# Steps to Create a Wheel File
## Follow these steps to create and distribute a Python package as a wheel file:

## 1. Create a Project Directory
 - **Create a folder (e.g., project_folder) to house your project files.**
## 2. Add Essential Files
 - **Inside the folder, create the following files:**
 
 - **README.txt** : A description of your project.
 - **LICENSE.txt** : Licensing information for your project.
 - **setup.py** : A Python script for package configuration.
 - **In setup.py** , import the setuptools package and use the setup() function. Include details like:
 
   **1. name**
   **2. description**
   **3. author**
   **4. version**
   **5. author_email**
   **6. packages**
   **7. install_requires, etc.**

### Example setup.py snippet:
   ```bash
   from setuptools import setup, find_packages
   
   setup(
       name="awaish_pkg",
       version="1.0",
       author="Your Name",
       author_email="your_email@example.com",
       description="A Python package for demonstration",
       packages=find_packages(),
       install_requires=[],
   )
   ```
## 3. Add Your Package Code
 - **Inside the main folder, create another folder (e.g., package_folder) to house your package code.**
 - **Inside this folder, create an __init__.py file and write your Python code.**
## 4. Build the Wheel File
 - **Open a terminal in the main folder (or navigate to it using your terminal/IDE).**
 - **Run the following command:**
   ```bash
   python setup.py sdist bdist_wheel
   ```

## 5. Locate the Wheel File
 - **After running the above command, a dist folder will be created.**
 - **Inside this folder, you will find the wheel file (e.g., awaish_pkg-1.0-py3-none-any.whl).**
## 6. Install the Wheel File
 - **Use the following command to install the wheel file:**
   ```bash
   pip install <path_to_wheel_file>
   ```

## Exampla :
  ```bash
  pip install dist/awaish_pkg-1.0-py3-none-any.whl
  ```

## 7. Use the Package
 - **After installation, you can import and use your package in Python:**
   ```bash
   import your_package_name
   ```




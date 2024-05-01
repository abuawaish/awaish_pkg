A wheel file install and use it...
## NOTE - open cmd in same folder where your wheel file exist or just copy the path of your wheel file and type the following command in terminal
                            pip install wheel_file_name(awaish_pkg-2.4-py3-none-any.whl)

## Steps to create a wheel file :
- step1 : create a folder(i.e. 1st folder)
- step2 : create three files in 1st folder such as readme.txt,
        Licence.txt and setup.py
        In setup.py file import setuptools package and use setup function (`from setuptools import setup`) 
        write your package description in setup()
        function such as name,description,author,version.
        aurthor_email,packages,install_requires and
        so on.......(1st folder)
- step3 : inside the 1st folder create another folder(i.e. 2nd folder)
        which consist __init__.py file, In this file
        write your code.

- step4 : open vscode or cmd or any python IDLE in first
         folder and go to terminal and type the following command : 
                `python setup.py sdist bdist_wheel`
        and hit enter
        Now we have successfully created our wheel file.
- step5 : go to the dist folder which have been created after running (`python setup.py sdist bdist_wheel`) command
- step6 : inside this folder there is a wheel file(`pkgawaish-0.2-py3-none-any.whl`) something like this.
- step7 : now install this wheel file in your system with the help of pip(`pip insall wheel_file_name`).
        Now this package is ready to use you can use this package in your system by `import PACKAGE_NAME` command.




                            

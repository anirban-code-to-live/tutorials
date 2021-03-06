Steps used to create a virtual environment::

1. Make sure you’ve got Python & pip. <br>
	`` python --version ``
	`` python -m pip --version ``
	
  If pip is not installed or not up-to-date, you can install/upgrade using <br>
  	`` python3 -m pip install --user --upgrade pip``

2. Install virtualenv via pip:<br>
	`` python3 -m pip install --user virtualenv ``
	Test your installation:
	`` python3 -m virtualenv --version ``

3. Create a virtual environment for a project:<br>
	`` cd my_project_folder ``
	`` python3 -m venv env ``
	** It's a good idea to create the environment inside your project folder. You can name it anything (venv is standard)

  You can also use the Python interpreter of your choice (like python2.7).<br>
	`` virtualenv -p /usr/bin/python2.7 venv ``

4. To begin using the virtual environment, it needs to be activated:<br>
	`` source venv/bin/activate ``

5. If you are done working in the virtual environment for the moment, you can deactivate it:<br>
	`` deactivate ``
	This puts you back to the system’s default Python interpreter with all its installed libraries.

6. To delete a virtual environment, just delete its folder. (In this case, it would be rm -rf my_project.)

7. In order to keep your environment consistent, it’s a good idea to “freeze” the current state of the environment packages. To do this, run:<br>
	`` pip freeze > requirements.txt ``

8. This will create a requirements.txt file, which contains a simple list of all the packages in the current environment, and their respective versions. You can see the list of installed packages without the requirements format using pip list. Later it will be easier for a different developer (or you, if you need to re-create the environment) to install the same packages using the same versions:<br>

	`` pip install -r requirements.txt ``
	** This can help ensure consistency across installations, across deployments, and across developers.

9. Lastly, remember to exclude the virtual environment folder from source control by adding it to the ignore list.


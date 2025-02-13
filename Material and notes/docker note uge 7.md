For using docker containers, the user sometimes need to build 
they own images, even if it's based on a existing template.

one example of a use for this could be using the a "Python3" image
as a starting point, then use the package manager (pip)
to download "Flask"{1}, Flask is an framework for hosting website.

so for this example, I created a folder called "Flask-docker"
 
inside this folder are 3 files
->
	app.py
	Dockerfile
	requirements.txt

and a folder venv, which is created by python3 to host a virtual enviorment,
basiccally a seperat installation of python3 that is contained.

inside this venv folder there's a Scripts folder which has a activation script.
by runnng this script, you are now working inside that instance of python3.
this will be usefull since our docker image will need not only python, but
the package for flask. after installing the package, use the "pip list" 
command to note what packages should be put into the requirements.txt file
thereby the dockerfile know what are the requirement for the program to run.

the app.py contains the minium code needed to for hosting the html page, on the local-host
lastly the dockerfile gives the instructions to creating the working docker image.


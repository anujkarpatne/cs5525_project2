# CS5525 Project2 - Getting Started on Using rlogin.cs.vt.edu

Open a terminal on your machine, type in:

`ssh -L 8000:localhost:xxxx username@rlogin.cs.vt.edu`

Replace "xxxx" with an arbitrary 4 digits number, for example 8765. Replace "username" with your vt id, for example "kklein".
After login,execute the following command line by line:
	
```
mkdir COVID_clustering
cd COVID_clustering
python3 -m venv python3-virtualenv
source venv/bin/activate
python3 -m pip install jupyter --user
python3 -m pip install pandas sklearn searborn numpy bokeh --user
jupyter lab --port xxxx 
```

You may get some messages like:
```
    To access the notebook, open this file in a browser:
        file:///C:/Users/bujie/AppData/Roaming/jupyter/runtime/nbserver-9476-open.html
    Or copy and paste one of these URLs:
        http://localhost:xxxx/?token=c3c6074b04bff28d83fdc5d0ede431c0a121774816db49b2
     or http://127.0.0.1:xxxx/?token=c3c6074b04bff28d83fdc5d0ede431c0a121774816db49b2
```

It shows your jupyter server is running at port xxxx and your token will be the string after "token=". The xxxx value should be the same as the number you pick. Otherwise, you may need to pick another value for xxxx and login again.Follow the following:

- Close the terminal and open a new one.
- Use a new value of xxxx, type in:

`ssh -L 8000:localhost:xxxx username@rlogin.cs.vt.edu`

- After login,execute the following commands line by line:
	
```
cd COVID_clustering
source venv/bin/activate
jupyter lab --port xxxx 
```

Note that the above three lines are the code you need to execute each time you login into the remote machine.On your PC, open `http://localhost:xxxx` in a browser.For the first time login, you may be asked to provide token to create a password.

You may be able to see the UI of Jupyter Lab. By default, it has a side bar with file explorer at left and a notebook editor at right.

You should be able to upload the notebook "covid-19-literature-clustering.ipynb" by draggin it into the file explorer in the Jupyter Lab UI.

Double click to open it in the notebook editor.Download the dataset into your machine from Google Drive:
https://drive.google.com/file/d/1IC0s9QoBLWFN9tRI-z2QbJJWgngfAm8w/view

Drag the downloaded "CORD-19-research-challenge.zip" into the file explorer in your Jupyter Lab UI. It will start uploading the file into the remote server. 

It might take a while and please make sure you have stable network connection.Click on the "+" button on top of the file explorer and choose terminal in the popped out tab. Then type in the following:
	
```
cd COVID_clustering
unzip CORD-19-research-challenge.zip
```
Finally, you should be able to run your notebook.

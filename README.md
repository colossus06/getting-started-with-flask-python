# getting-started-with-flask-python

## Create and run a virtual env


```
sudo apt install python-virtualenv
python3 -m venv <name of environment>
source <name of environment>

```
## Create a directory for your app

```
cd <where-you-want-to>
mkdir flask-app
cd flask-app
touch blog.py
code blog.py
```

**Note**: You might want to name your app anything other thatn `flask.py` to avoid the following error:

`Error: Failed to find Flask application or factory in module 'flask'. Use 'flask:name' to specify one.`
You can find a thread here for more details: [stackoverflow](https://stackoverflow.com/questions/57718786/error-launching-flask-app-with-error-failed-to-find-flask-application)

## Install flask

```
pip install Flask
```

## Writing the code




```
from flask import Flask, render_template, url_for


app = Flask(__name__)
```

```
@app.route('/')
@app.route('/home')
def home():
    return render_template('index.html')


```

You may want to create an index.html file as shown in the file structure of the image below.

![image](https://user-images.githubusercontent.com/96833570/189882990-901bbdec-1d08-475a-8369-b10017e22b6a.png)

Or you can simply replace the above `return render_template('index.html')` statement with the following:

`return "Hello World"`

```

if __name__ == "__main__":
    app.run(debug=True)

```
By specifying the debug=True, you won't need to stop flask server and set environment variables again and again. 

## Running the flask app

To run the flask app type:

`python blog.py`



![image](https://user-images.githubusercontent.com/96833570/189883691-f666eb07-f9c1-40cd-bc41-7833bde92c68.png)


![image](https://user-images.githubusercontent.com/96833570/189883824-5516a8a0-2267-4b90-bba0-49ddd2b92c4b.png)

And you're good to go!


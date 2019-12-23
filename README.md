# CherryPy

## Installation
CherryPy is a pure Python library. This has various consequences:

  - It can run anywhere Python runs
  - It does not require a C compiler
  - It can run on various implementations of the Python language: CPython, IronPython, Jython and PyPy

## Requirements
CherryPy does not have any mandatory env requirements. Python-based distribution requirements are installed automatically by pip. However certain features it comes with will require you install certain packages. To simplify installing additional dependencies CherryPy enables you to specify extras in your requirements (e.g. cherrypy[json,routes_dispatcher,ssl]):

  - doc – for documentation related stuff
  - json – for custom JSON processing library
  - routes_dispatcher – routes for declarative URL mapping dispatcher
  - ssl – for OpenSSL bindings, useful in Python environments not having the builtin ssl module
  - testing
  - memcached_session – enables memcached backend session
  - xcgi

## Supported python version
CherryPy supports Python 3.5 through to 3.8.

## Installing
CherryPy can be easily installed via common Python package managers such as setuptools or pip.
  
<pre><code>$ easy_install cherrypy</pre></code>
<pre><code>$ pip install cherrypy</pre></code>

You may also get the latest CherryPy version by grabbing the source code from Github:

<pre><code>$ git clone https://github.com/cherrypy/cherrypy
$ cd cherrypy
$ python setup.py install
</pre></code>

## Test your installation
CherryPy comes with a set of simple tutorials that can be executed once you have deployed the package.

<pre><code>$ python -m cherrypy.tutorial.tut01_helloworld</pre></code>

Point your browser at http://127.0.0.1:8080 and enjoy the magic.

Once started the above command shows the following logs:

<pre><code>[15/Feb/2014:21:51:22] ENGINE Listening for SIGHUP.
[15/Feb/2014:21:51:22] ENGINE Listening for SIGTERM.
[15/Feb/2014:21:51:22] ENGINE Listening for SIGUSR1.
[15/Feb/2014:21:51:22] ENGINE Bus STARTING
[15/Feb/2014:21:51:22] ENGINE Started monitor thread 'Autoreloader'.
[15/Feb/2014:21:51:22] ENGINE Serving on http://127.0.0.1:8080
[15/Feb/2014:21:51:23] ENGINE Bus STARTED</pre></code>

We will explain what all those lines mean later on, but suffice to know that once you see the last two lines, your server is listening and ready to receive requests.

## Run it
During development, the easiest path is to run your application as follow:

<pre><code>$ python myapp.py</pre></code>

As long as myapp.py defines a “__main__” section, it will run just fine.

### cherryd
Another way to run the application is through the cherryd script which is installed along side CherryPy.

<pre><code><strong>Note:</strong>
This utility command will not concern you if you embed your application with another framework.</pre></code>

### Command-Line Options
<strong>-c, --config</strong><br>
Specify config file(s)

<strong>-d</strong><br>
Run the server as a daemon

<strong>-e, --environment</strong><br>
Apply the given config environment (defaults to None)

<strong>-f</strong><br>
Start a FastCGI server instead of the default HTTP server

<strong>-s</strong><br>
Start a SCGI server instead of the default HTTP server

<strong>-i, --import</strong><br>
Specify modules to import

<strong>-p, --pidfile</strong><br>
Store the process id in the given file (defaults to None)

<strong>-P, --Path</strong><br>
Add the given paths to sys.path

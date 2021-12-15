# A function for setting up aiohttp web server

Web server based on aiohttp library is, IMHO, more modern and flexible than 
others. So, as I use it pretty often, I decided to customize it for myself.

You can run aiohttp web server as simple as

```
from aiohttp-setup import setup

setup()
```

There are following features:

* static files are enable; the default directory where they are
located is `./public` directory;
* you can pass async services to the setup as tuples (start-function and stop-function);
* you can pass routes, that can be organized in separate module.

The function has no position parameter and some keyword-parameters:

```
def setup(host='localhost', port=8080, services=[], routes=None, 
        static_dir='public', index_file='index.html', root_path='/', 
        show_index=True):
```

I mean their names describes themselves, but, I hope to write 
some documentation in future :) .


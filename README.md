# whttp

Command line interface and Python library wrapper for the [winhttp] library

# Motivation

In some organizations there is a wide variety of http proxies configurations and authentications (SmartCard SSL Certificates; Kerberos; etc) which makes it very hard to use the most common http client utilities and Python http libraries.

In such cases, it is usually easier to rely on a Windows native HTTP tecnhology to handle the proxy configuration single sign-on authentication on your behalf.

This tool/library uses the [winhttp] library.


[winhttp]: https://docs.microsoft.com/en-us/windows/win32/winhttp/about-winhttp

[![PyPi](https://img.shields.io/pypi/v/whttp.svg?style=flat-square)](https://pypi.python.org/pypi/whttp)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg?style=flat-square)](https://github.com/ambv/black)

# How to install
```bat
pip install whttp
```

# How to use (CLI)
whttp https://www.example.org/

# How to use (Python Library)
```python
from whttp import HTTPClient
client = HTTPClient()
reply = client.get('https://www.example.org/')
print(reply.text)
```

# Other options

If you want to use some more Python friendly http library please consider the alternative method of introducing a local http proxy, for example [Px]

[Px]: https://github.com/genotrance/px

# Django SSFS (Simple Static File Storage)

## Why?

We build a lot of projects with Django.  Often we're deploying to Heroku which has an ephemeral file system.  We usually just want to get our site up and running.

This project helps by using a one-liner to configure Django's **static media storage** (e.g. user file uploads that aren't part of the codebase).


## Installation

First, install the package.

`pip install django-simple-static-file-storage`

Then, get your API key.  At the moment, we generate the API key's manually.  DM us on Twitter for more information [@matix_io](https://twitter.com/matix_io).

Finally, set up the storage as follows:

```python
import simple_static_file_storage
simple_static_file_storage.configure(YOUR_API_KEY)
from simple_static_file_storage import * # yes, this 2nd import is required
```
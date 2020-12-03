<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/requests-etag-cache.svg?maxAge=3600)](https://pypi.org/project/requests-etag-cache/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/requests-etag-cache.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/requests-etag-cache.py/actions)

### Installation
```bash
$ [sudo] pip install requests-etag-cache
```

#### How it works
```
$REQUESTS_ETAG_CACHE/<url_hash>
```

`$XDG_CACHE_HOME/requests-etag-cache/<url_hash>` by default

#### Examples
```python
import requests
import requests_etag_cache

r = requests.get('https://pypi.org/project/requests/')
if not requests_etag_cache.uptodate(r):
    ...
    requests_etag_cache.save(r)
```

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>

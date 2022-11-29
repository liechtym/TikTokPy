<h1 align="center">TikTokPy</h1>
<div align="center">
    <a href="https://pypi.org/project/tiktokapipy/">
        <img src="https://img.shields.io/pypi/v/tiktokapipy?style=flat-square&logo=pypi">
    </a>
    <a href="https://www.python.org">
        <img src="https://img.shields.io/badge/python-3.8+-blue.svg?style=flat-square&logo=python">
    </a>
    <a href="https://pypi.org/project/tiktokapipy/">
        <img alt="GitHub" src="https://img.shields.io/github/license/Russell-Newton/TikTokPy?style=flat-square">
    </a>
    <br>
    <a href="https://github.com/Russell-Newton/TikTokPy/actions/workflows/tox.yml">
        <img src="https://img.shields.io/github/workflow/status/Russell-Newton/TikTokPy/Unit%20Tests?style=flat-square&logo=github">
    </a>
    <a href='https://tiktokpy.readthedocs.io/en/latest/?badge=latest'>
        <img src='https://readthedocs.org/projects/tiktokpy/badge/?version=latest&style=flat-square' alt='Documentation Status' />
    </a>
</div>

**Extract data from TikTok without needing any login information or API keys.**

## Table of Contents

* [Getting Started](#getting-started)
    * [Installation](#installation)
    * [Quick Start Guide](#quick-start-guide)
* [Documentation](#documentation)

## Getting Started

### Installation

Install the ``tiktokapipy`` package (or add it to your project requirements) and set up Playwright:

```shell
pip install tiktokapipy
python -m playwright install
```

### Quick Start Guide

TikTokPy has both a synchronous and an asynchronous API. The interfaces are the same, but the asynchronous API
requires awaiting of certain functions and iterators.

Both APIs must be used as context managers. To get video information in both APIs:

<table>
<tr>
<th>Synchronous</th>
<th>Asynchronous</th>
</tr>
<tr>
<td>

```py
from tiktokapipy.api import TikTokAPI

with TikTokAPI() as api:
    video = api.video(video_link)
    ...
```

</td>
<td>

```py
from tiktokapipy.async_api import AsyncTikTokAPI

async with AsyncTikTokAPI() as api:
    video = await api.video(video_link)
    ...
```

</td>
</tr>
</table>

More examples can be found in the [documentation](https://tiktokpy.readthedocs.io/en/latest/users/usage.html#examples).

> **Warning**
>
> Scraping will not always work on the first try. Sporadic network and loading issues could cause extraction to fail.
> Look at the documentation for the
> [API parameters](https://tiktokpy.readthedocs.io/en/latest/generated/reference/tiktokapipy.api.TikTokAPI.html#tiktokapipy.api.TikTokAPI)
> to see what options can help with this.

## Documentation

You can view the full documentation on [Read the Docs](https://tiktokpy.readthedocs.io/en/latest/).

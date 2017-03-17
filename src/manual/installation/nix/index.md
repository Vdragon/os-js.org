---
title: Install OS.js on NIX
layout: layout.html
---

# Install OS.js on NIX

This are the instructions on how to install on Linux and BSD platforms.

## Dependencies

- Node and npm
- Git (recommended)

---

## Manual (recommended)

To install manually, simply run these commands:

```bash
$ git clone https://github.com/os-js/OS.js.git
$ cd OS.js
$ npm install --production
$ node osjs build
```

You can download and extract a zip-file instead of using `git`, but is not recommended as it makes the update process harder.

---

## Automated

Download and run the installer in your shell:

```bash
$ curl -sS https://www.os.js.org/installer | sh
```

---

## Running

When you have [started a server](/manual/server), simply navigate to [http://localhost:8000](http://localhost:8000) (port 8000 is default).

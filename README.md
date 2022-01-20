# cde-manifest
Repo manifest for Cutefish Desktop Environment.

## Usage

### 1. Install repo to your machine.
Note that Git and Python 3.x is required and should be accessible via `/bin/python`.

On Debian/Ubuntu, use apt to install Python 3.
``` shell
sudo apt install -y python3 python-is-python3
```

Then install `repo` via these commands:
``` shell
mkdir ~/bin
cd ~/bin
curl https://mirrors.tuna.tsinghua.edu.cn/git/git-repo -o repo
chmod +x repo
```

After a relogin, `repo` should be available in PATH.

### 2. Init repo

You only have to do this once.

``` shell
mkdir ~/cutefish
cd ~/cutefish
repo init -u -b main
```

### 3. Sync actual code

```
repo sync
```

And you're good to go!

## Build all Cutefish components


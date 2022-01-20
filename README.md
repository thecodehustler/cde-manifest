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

Install dependencies (for Debian/Ubuntu only, credit to [chipo](https://my.oschina.net/chipo/blog/5077196))

``` shell
sudo apt install \
automake \
autotools-dev \
breeze-dev \
breeze-icon-theme-rcc \
build-essential \
cmake \
cryptsetup \
curl \
debhelper \
devscripts \
equivs \
extra-cmake-modules \
gettext \
git \
gcc \
g++ \
kirigami2-dev \
kwin-dev \
libboost-python-dev \
libcanberra-dev \
libcap-dev \
libcrypt-dev \
libdbus-1-dev \
libdbusmenu-qt5-dev \
libecm1-dev \
libfftw3-dev \
libfreetype6-dev \
libfontconfig1-dev \
libicu-dev \
libkdecorations2-dev \
libkf5config-dev \
libkf5bluezqt-dev \
libkf5codecs-dev \
libkf5coreaddons-dev \
libkf5configwidgets-dev \
libkf5doctools-dev \
libkf5filemetadata-dev \
libkf5globalaccel-dev \
libkf5guiaddons-dev \
libkf5i18n-dev \
libkf5iconthemes-dev \
libkf5idletime-dev \
libkf5kio-dev \
libkf5networkmanagerqt-dev \
libkf5package-dev \
libkf5parts-dev \
libkf5qqc2desktopstyle-dev \
libkf5service-dev \
libkf5syntaxhighlighting-dev \
libkf5screen-dev \
libkf5solid-dev \
libkf5widgetsaddons-dev \
libkf5windowsystem-dev \
libkpmcore-dev \
libmpv-dev \
libpam0g-dev \
libparted-dev \
libpolkit-agent-1-dev \
libpolkit-qt5-1-dev \
libpulse-dev \
libpwquality-dev \
libqapt-dev \
libqqc2breezestyle-dev \
libqt5x11extras5-dev \
libqt5xdg-dev \
libqt5sensors5-dev \
libqt5svg5-dev \
libqt5webkit5-dev \
libsm-dev \
libsystemd-dev \
libx11-dev \
libx11-xcb-dev \
libxcb1-dev \
libxcb-composite0-dev \
libxcb-damage0-dev \
libxcb-dpms0-dev \
libxcb-dri2-0-dev \
libxcb-dri3-dev \
libxcb-ewmh-dev \
libxcb-glx0-dev \
libxcb-icccm4-dev \
libxcb-image0-dev \
libxcb-keysyms1-dev \
libxcb-randr0-dev \
libxcb-record0-dev \
libxcb-shape0-dev \
libxcb-shm0-dev \
libxcb-util0-dev \
libxcb-util-dev \
libxcb-xfixes0-dev \
libxcursor-dev \
libxi-dev \
libxtst-dev \
libyaml-cpp-dev \
lintian \
modemmanager-qt-dev \
os-prober \
pkg-config \
pkg-kde-tools \
policykit-1 \
python3-dev \
qml-module-org-kde-kwindowsystem \
qml-module-qt-labs-platform \
qml-module-qt-labs-settings \
qml-module-qtqml \
qml-module-qtquick-controls2 \
qml-module-qtquick-dialogs \
qml-module-qtquick-layouts \
qml-module-qtquick-privatewidgets \
qml-module-qtquick-window2 \
qml-module-qtquick-shapes \
qml-module-qtquick2 \
qtbase5-dev \
qtbase5-private-dev \
qtdeclarative5-dev \
qtquickcontrols2-5-dev \
qttools5-dev \
qttools5-dev-tools \
sound-theme-freedesktop \
xserver-xorg-dev \
xserver-xorg-input-libinput-dev \
xserver-xorg-input-synaptics-dev
```

After a success sync, run this command under project root:

``` shell
bash ./build.sh
```

The build should start, and ask you for the root password to install the artifacts.

If you want to build without installing, pass `--no-install` to this script.

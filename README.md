# THIS IS NOT AN OFFICIAL INSTALLER - use at your own risk

This is an attempt to get the ubuntu sdk working on newer versions of ubuntu and other distros using lxd

The container includes the sdk libraries and also install qtcreator from upstream as the one in the ubuntu archives
doesn't work so great. A desktop file will be created so you can launch qtcreator from your applications menu.



## Getting Setup

Clone this repo

```
git clone https://github.com/dpniel/ubports-sdk-setup
cd ubports-sdk-setup
```

Then to create a development container run the following


NOTE: By default the container targets xenial 16.04. To target a different release you can use the `--target ubuntu:$VERSION` option

```
./ubports-sdk-setup -d
```

or if you want a cross build container

```
./ubports-sdk-setup -c
```

If you want to change the default install location of qtcreator you can set the `QTCREATOR_INSTALL_DIR=/custom/path` env var.

To use a different name for a container just pass it to the setup script `./ubports-sdk-setup -d mycontainer`



Still todo

* [] Make this README better
* [] USB Passthrough
* [] Automate enablement of sound via paprefs on host (is this possible)
* [] Support multiple containers - currently qtcreator only get's configured for the first dev container. 

![MOTD screenshot](readme-img.png)

## Usage

### Running
Clone the repository:
```shell
git clone https://github.com/tywhisky/motd.git
```

Then run `motd.sh`:
```shell
./motd/motd.sh
```

At last:
```shell
ln -S ./motd/motd.sh /etc/update-motd.d/10-motd
```

### Requirements
In order to run all the available modules the following programs are required:

* [`figlet`](http://www.figlet.org/)
* [`curl`](https://curl.se/)
* [`bc`](https://www.gnu.org/software/bc/)
* [`fortune`](https://software.clapper.org/fortune/)
* [`lolcat`](https://github.com/busyloop/lolcat)

This list excludes the obvious ones, like [`tmux`](https://github.com/tmux/tmux) for `tmux` module.

If any program requried by the given module is missing (or any other error occurs), it will fail silently, i.e. the module just won't be shown at all.

## Hacking
To add a new module you can create a new script in `modules` directory.
For the output to be properly formatted it has to use `print_columns` function from `framework.sh`, please refer to the existing modules.

Module files have to start with a two digit number followed by a hyphen. You may disable modules by simply rename the module file.

## Credits
This MOTD is hugely inspired by [this repo](https://github.com/bcyran/fancy-motd) by Bazyli Cyran.

Generate message from a image by [this repo](https://github.com/RoBorg/MOTD) by RoBorg.

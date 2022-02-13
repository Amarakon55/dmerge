# Dmerge – Dmenu Emerge

Dmerge is a simple command-line utility to Emerge and Unmerge packages using Dmenu.
The usage is very simple:
* `$ dmerge` – search for and emerge packages
* `$ dmerge --depclean` or `$ dmerge -c` – search for and deplean packages
* `$ dmerge --unmerge` or `$dmerge -C` – search for and unmerge packages
* `$ dmerge <atom>` – emerge \<atom\>, search for and emege packages

etc...

## Dependencies
1. portage
1. eix or portage-Utils
    * eix is recommended because it is faster and has more details.

## (Un)Installation
### Universal
#### Installation
##### Latest Git Master (Bleeding Edge)
1. Git clone the repository.
* `$ git clone https://github.com/Amarakon55/dmerge`
2. Change working directory to *dmerge*.
* `$ cd dmerge`
3. Install Dmerge using the Makefile
* `# make install`
#### Uninstallation
##### Latest Git Master (Bleeding Edge)
1. Change working directory to *dmerge*.
* `$ cd dmerge`
2. Uninstall Dmerge using the Makefile
* `# make uninstall`

### Gentoo
#### Installation
##### Latest Git Master (Bleeding Edge)
1. Add my personal [Gentoo overlay](https://github.com/Amarakon55/amarlay) using [eselect-repository](https://packages.gentoo.org/packages/app-eselect/eselect-repository)
* `# eselect repository add amarlay git https://github.com/Amarakon55/amarlay`
2. Sync my personal [Gentoo overlay](https://github.com/Amarakon55/amarlay) using `emerge`
* `# emerge --sync amarlay`
3. Emerge the Dmerge package
* `# emerge x11-misc/dmerge` or `# emerge dmerge`
#### Uninstallation
##### Latest Git Master (Bleeding Edge)
1. Unmerge the Dmerge package
* `# emerge -c x11-misc/dmerge` or `# emerge -c dmerge`
2. (Optional) Remove my overlay
* `# eselect-repository remove -f amarlay`
3. (Optional) Sync using `emerge`
* `# emerge --sync`

# package: A portable package manager

Are you tired of using different commands of package managers on different OS(e.g. `yum` for CentOS/RedHat/Fedora, `apt` for Ubuntu/Debian, `brew`/`port` for macOS)? If so, `package` will save you by providing unify commands(e.g. `install` `uninstall`) in most cases.

## Supported backend package managers

- `dnf` for CentOS/RedHat/Fedora
- `yum` for CentOS/RedHat/Fedora
- `apt` for Ubuntu/Debian
- `brew` for macOS
- `opkg` [Entware](https://github.com/Entware/Entware), for Synology DSM or other embedded devices
- `apk` for Alpine Linux

## Installation

### Alpine Linux

```shell
wget -O /usr/local/bin/package https://raw.githubusercontent.com/muyinliu/package/master/package
sed -i "s/bash/sh/g" /usr/local/bin/package
chmod +x /usr/local/bin/package
```

Note: default shell of [Alpine Linux](https://alpinelinux.org/) is `ash`(Almquist shell) in [busybox](https://www.busybox.net/), NOT `bash`, so have to replace `bash` with `sh`

Note: by default [Alpine Linux](https://alpinelinux.org/) contains download tool `wget`, NOT `curl`

### Other Linux & macOS

```shell
curl -o /usr/local/bin/package https://raw.githubusercontent.com/muyinliu/package/master/package
chmod +x /usr/local/bin/package
```

## `package` help doc

```shell
package help
```
=>
```=>
Usage: package <command>

commands:
  install <package> [<package>]     install package
  add <package> [<package>]         alias of command install
  uninstall <package> [<package>]   uninstall package
  remove <package> [<package>]      alias of command uninstall
  delete <package> [<package>]      alias of command uninstall
  purge <package> [<package>]       uninstall package with its config files
  update                            update metadata of packages
                                      or package manager itself(e.g. brew)
  upgrade <package> [<package>]     upgrade package
  cleanup                           auto remove unneeded packages
  autoremove                        alias of command cleanup
  list                              list all available packages
  list-installed                    list installed packages
  list-upgradable                   list upgradable packages
  list-update                       alias of command list-upgradable
  list-updates                      alias of command list-upgradable
  search <pattern>                  search package
  find <pattern>                    alias of command search
  show <package> [<package>]        show info of package
  info <package> [<package>]        alias of command command show
  files <package> [<package>]       show files of package
  provides <file>                   find package providing the file
  depends <package>                 show dependencies of package
  rdepends <package>                show packages depend on package
                                      (reverse dependencies)
  backend                           show backend package manager
  help                              show this help doc

IMPORTANT NOTE: Only support following backend package managers: dnf, yum, apt, brew(for macOS), opkg(Entware for embedded devices) and apk(for Alpine Linux)
```

## License

MIT (See LICENSE file for details).

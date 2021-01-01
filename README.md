# package: A portable package manager

Are you tired of using different commands of package managers on different OS(e.g. `yum` for CentOS/RedHat/Fedora, `apt` for Ubuntu/Debian, `brew`/`port` for macOS)? If so, `package` will save you by providing unify commands(e.g. `install` `uninstall`) in most cases.

## Installation

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
  install <package>      install package
  add <package>          alias of command install
  uninstall <package>    uninstall package
  remove <package>       alias of command uninstall
  delete <package>       alias of command uninstall
  purge <package>        uninstall package with its config files
  update                 update metadata of packages or package manager itself(e.g. brew)
  upgrade <package>      upgrade package
  cleanup                auto remove unneeded packages
  autoremove             alias of command cleanup
  list                   list all available packages
  list-installed         list installed packages
  search <pattern>       search package
  find <pattern>         alias of command search
  show <package>         show info of package
  info <package>         alias of command command show
  files <package>        show files of package
  provides <file>        find package providing the file
  depends <package>      show dependencies of package
  rdepends <package>     show packages depend on package(reverse dependencies)
  help                   show this help doc
```

## License

MIT (See LICENSE file for details).

# webOS apps

Homebrew Channel catalog for the webOS app forks on [z3d6380](https://github.com/z3d6380).

Add this URL in Homebrew Channel, under Settings, Add repository:

```
https://raw.githubusercontent.com/z3d6380/webos-apps/main/apps.json
```

`apps.json` is the catalog the TV reads. `sources.json` maps each package to its fork and its upstream.

A GitHub fork does not include the upstream release files. Until a fork publishes its own manifest, that package's `manifestUrl` still points at the upstream release, so Homebrew installs the upstream IPK. After you publish a manifest on the fork, change that one `manifestUrl` to:

```
https://github.com/z3d6380/<fork>/releases/latest/download/<id>.manifest.json
```

## Left out on purpose

GitHub allows one fork per repository network. `youtube-webos` tracks `webosbrew/youtube-webos`. The NicholasBly and foxi69 trees are the same network, so they are not separate forks. `lg-hue-sync` tracks `adeze/lg-hue-sync`. `aurora-tv` is the one fork of the Moonlight network.

These were not forked: rooting tools, StremCompat, CloudStream, Stash, and the game ports that need copyrighted game assets. Apps that exist only on repo.webosbrew.org have no Git repository to fork. Homebrew Channel itself is not in this catalog.

The G5 apps and the webOS 25 DTS package are forked and omitted from `apps.json`. This set is a C3 on webOS 11.

Several launchers in the catalog replace LG Home when you install them. Adding the repository only lists them.

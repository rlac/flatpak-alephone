# AlephOne Flatpak

This is a [Flatpak](https://flatpak.org/) build of [AlephOne](https://alephone.lhowon.org/) as a base app, plus [Marathon](https://alephone.lhowon.org/games/marathon.html), [Marathon 2](https://alephone.lhowon.org/games/marathon2.html), and [Marathon Infinity](https://alephone.lhowon.org/games/infinity.html) scenario Flatpak builds.

## Installation

For now, you can build locally. Ensure your system has Flatpak installed, then:

```bash
flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
flatpak install org.flatpak.Builder org.freedesktop.Platform//20.08 org.freedesktop.Sdk//20.08
flatpak run org.flatpak.Builder --install --user builddir org.lhowon.AlephOne.BaseApp.json --force-clean
flatpak run org.flatpak.Builder --install --user builddir org.lhowon.AlephOne.Marathon.json --force-clean
flatpak run org.flatpak.Builder --install --user builddir org.lhowon.AlephOne.Marathon2.json --force-clean
flatpak run org.flatpak.Builder --install --user builddir org.lhowon.AlephOne.MarathonInfinity.json --force-clean
```

To uninstall:

```bash
flatpak remove org.lhowon.AlephOne
```

## Playing

Desktop launcher files aren't available yet. Run the games from the command line with one of the following:

```bash
flatpak run org.lhowon.AlephOne.Marathon
flatpak run org.lhowon.AlephOne.Marathon2
flatpak run org.lhowon.AlephOne.MarathonInfinity
```
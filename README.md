## Flatpak
The TUMexam client can be built and installed using Flatpak.

### Requirements
#### Fedora
```
sudo dnf install flatpak flatpak-builder
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.gnome.Sdk/43 org.gnome.Platform/43
```

#### Debian/Ubuntu
```
sudo apt install flatpak flatpak-builder
flatpak install flathub org.gnome.Sdk/43 org.gnome.Platform/43
```

### Building
```
git clone https://github.com/flathub/de.tumexam.cli.git
cd de.tumexam.cli
flatpak-builder --force-clean flatpak_build_dir de.tumexam.cli.yml
```

### Installing
```
flatpak-builder --user --install --force-clean flatpak_build_dir de.tumexam.cli.yml
```

### Uninstalling
```
flatpak uninstall de.tumexam.cli
```

### Executing
```
flatpak run de.tumexam.cli
```

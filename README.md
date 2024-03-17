# Install ruby and bundler

## Ubuntu

```sh
sudo apt-get install ruby-full build-essential zlib1g-dev
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
gem install bundler
```

## Arch Linux (Manjaro)

### Install Ruby

Wenn rbenv und ruby-build nicht vorhanden sind. Pakete über AUR im package manager installieren.

```sh
sudo pacman -Syu
sudo pacman -S rbenv ruby-build
```

```sh
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bashrc
source ~/.bashrc
```

Ruby Version für GitHub Pages installieren:
```sh
rbenv install 2.7.4
rbenv global 2.7.4
```

### Install Bundler
```sh
gem install bundler -v 2.4.22
gem install json
```


# Build Project
Navigate to the project and install dependencies.

```sh
bundle install
```

# Run Project
```sh
bundle exec jekyll serve
```
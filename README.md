# Circos

http://circos.ca

## Breakdown of the README.md file
1. [Setup](#Setup-on-Mac)

## Setup on Mac
1. Download circos from [here.](http://circos.ca/software/download/circos/)
2. unpack the circos file: tar xvfz circos-version
3. Install Homebrew for Mac
  a. /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  b. echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.bash_profile #can change this with the command output by your 
  c. eval "$(/opt/homebrew/bin/brew shellenv)"
4. brew install pkg-config
5. Install cpanm:
  a. curl -L https://cpanmin.us | perl - App::cpanminus --sudo
6. cpanm ExtUtils::PkgConfig --sudo
7. brew install libgd
8. export PKG_CONFIG_PATH=/path/to/pkgconfig
9. cd circos-version/bin
10. Installing required Modules
  a. sudo cpan
  b. cpanm Config::General Font::TTF::Font Math::Bezier Math::VecStat Readonly Set::IntSpan Text::Format
  c. cpanm --force GD::Polyline --sudo
  d. Install other modules that haven't changed status to okay when running: circos -modules
  

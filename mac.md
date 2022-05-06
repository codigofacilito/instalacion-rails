Instalación rbenv

```bash
brew install rbenv ruby-build
```

Agregando rbenv al path

```bash
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.zshrc
source ~/.zshrc
```

Instalación de ruby 3

```bash
rbenv install 3.1.1
rbenv global 3.1.1
```

Instalación rails

```bash
gem install rails -v 7.0.2.3
rbenv rehash
```

Comando final 

```bash
rails -v
```
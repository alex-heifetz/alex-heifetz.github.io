# 01 Raycast
[Raycast - Supercharged productivity](https://www.raycast.com/#)
Заходим в **System Preferences** → **Keyboard** → **Spotlight** → отключаем hotkey'и.
Заходим в настройки **Rectangle** и включаем hotkey'и для **Window Management** → **Rectangle**

# 02 Warp
[Скачать](https://app.warp.dev/get_warp)

# 03 Oh My Zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
compaudit | xargs chmod g-w,o-w
```

### Настройка OMZ

Скопировать .zshrc в домашнюю папку
```bash
cp ~/SynologyDrive/MacOS/zshrc ~/.zshrc
```

# 04 Homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/heifetz/.zprofile eval "$(/opt/homebrew/bin/brew shellenv)"
```

### Разные утилиты
```bash
brew install pv
brew install mysql-client
echo 'export PATH="/opt/homebrew/opt/mysql-client/bin:$PATH"' >> ~/.zshrc
brew install graphviz
brew install postgresql
echo 'export PATH="/opt/homebrew/opt/postgresql@14/bin:$PATH"' >> ~/.zshrc
```

### PHP
```bash
brew install php 
brew install php@8.1
```
### Переключение версии PHP
```bash
brew unlink php && brew link --overwrite php@8.1
```

### NVM
```bash
brew install nvm 
```
В .zshrc добавить то что написано в результате

# JetBrains Toolbox
[Ссылка](https://www.jetbrains.com/ru-ru/toolbox-app/)

# Sublime Text
Установить с официального [сайта](https://www.sublimetext.com/download).

Копируем чтобы можно было запускать через `subl`

```bash
echo 'export PATH="/Applications/Sublime Text.app/Contents/SharedSupport/bin:$PATH"' >> ~/.zprofile
```

# Composer
```bash
curl -sS https://getcomposer.org/installer | php
sudo mv composer.phar /opt/homebrew/bin/composer
```

# Остальное
## Ключи

```bash
mkdir ~/.ssh
cp ~/SynologyDrive/MacOS/ssh/id_rsa ~/.ssh/id_rsa
cp ~/SynologyDrive/MacOS/ssh/id_rsa.pub ~/.ssh/id_rsa.pub
sudo chmod 600 ~/.ssh/id_rs*
```

## Быстрые авто-клики

**System Settings** → Keyboard

**Key repeat rate** и **Delay until repeat* на максимум.

## Выключаем ненужные заметки в углу экрана

**System Settings** → search **Hot Corners Shortcuts**

Выключаем все.

## Home and End keys

```shell
mkdir ~/Library/KeyBindings && \
touch ~/Library/KeyBindings/DefaultKeyBinding.dict && \
echo '{
    "\UF729"   = moveToBeginningOfLine:; // home
    "\UF72B"   = moveToEndOfLine:; // end
    "$\UF729"  = moveToBeginningOfLineAndModifySelection:; // shift-home
    "$\UF72B"  = moveToEndOfLineAndModifySelection:; // shift-end
    "^\UF729"  = moveToBeginningOfDocument:; // ctrl-home
    "^\UF72B"  = moveToEndOfDocument:; // ctrl-end
    "^$\UF729" = moveToBeginningOfDocumentAndModifySelection:; // ctrl-shift-home
    "^$\UF72B" = moveToEndOfDocumentAndModifySelection:; // ctrl-shift-end
}' > ~/Library/KeyBindings/DefaultKeyBinding.dict
```

## Приложения

[Keyboard Pilot](https://apps.apple.com/ru/app/keyboard-pilot/id402670023?mt=12) Есть в App Store
[BitWarden](https://bitwarden.com/download/) Есть в App Store
[HiddenBar](https://apps.apple.com/us/app/hidden-bar/id1452453066?mt=12) Есть в App Store
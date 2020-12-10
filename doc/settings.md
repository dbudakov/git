### Настройка рабочего окружения

`/etc/gitconfig` - является файлом настроек для всех пользователей настраивается с помощью `git config --system`
`~/.gitconfig` - является пользовательским файлом настроек настраивается с помощью `git config --global`
`.git/config` - является локальным файлом настроек, только для данного репозитория, настройка из репозитория по команде `git config`

#### Идентификатор

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

#### Выбор редактора для коммита

```sh
git config --global core.editor emacs
```

#### Список настроек

```sh
# будут считаны все файлы конфигураций
git config --list
```

#### Значение конкрентного параметра

```sh
# git config <key>
git config user.name
```

#### Исключения

```sh
./.git/info/exclude # частный случай
./.gitignore
git config --global core.excludesfile ~/.gitignore_global # задание файла gitignore
```

Дополнительно: [github](https://github.com/github/gitignore)

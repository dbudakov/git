#### Инициализация репозитория

```sh
git init
```

#### Клонирование репозитория

```sh
# клонирование в текущий каталог
git clone https://github.com/libgit2/libgit2
# клонирование в указаный каталог mylibgit
git clone https://github.com/libgit2/libgit2 mylibgit
```

#### Варианты протоколов

- https://
- git://
- user@server:path/to/repo.git

#### Рабочие команды

`git chekout <file>` - to discard changes in working directory
`git restore [<file>|"./"]` - restore file or all repo
`git restore --staged <file>` - откат индексации файла
`git rm --cached <file>` - удалить файл из отслеживаемых
`git add <file> `- проиндексировать файл или добавить в отслеживаемым, а также пометить файл с конфликтом как разрешенный для слияния
`git commit <file>` - зафиксировать файл
`git commit -a ` - commit without staged, tracked files
`git status` - состояние файлов в репозитории
`git status -s [ --short ]`
`git reset HEAD` - to unstage
`git diff` - change list
`git diff --staged` - staged changes with last commit version
`git diff --cached` - also `-- staged`

`git log` - просмотр истории
`git log -p -2` - выводит два последних коммита и показывает разницу внесенную каждым коммитом
`git log --stat` - краткая статистика по каждой версии
`git log --pretty=oneline` - изменяет формат вывода, доступные варианты(`short`, `full`, `fuller`)
`git log --pretty=format: "%h - %an, %ar : %s"` - форматируемый вывод лога
`git log --pretty=format: "%h %s" --graph` - графическое ветвление

Всего два типа тегов - легковесные(lightweight)(указательл на коммит) и снабженные комментарием(annotated)(есть cheksum, есть контакты автора тега, дата, комментарий)
`git tag` - просмотр всех тегов
`git tag -a v1.0 -m 'my version 1.4'` - создание annotated tags
`git tag v0.1` - создание lightweight tags
`git tag v0.1 c7aa519` - создание lightweight tags для определенного коммита
`git push origin <tag_name>` - отправка тега на удаленный репозиторий
`git push origin --tags` - отправка всех тегов

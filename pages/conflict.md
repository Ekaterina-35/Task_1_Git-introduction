## Разрешение конфликтов слияния

### Конфликты изменения строк

Если несколько человек редактировали файл **имя файла.md** в одних и тех же строках в разных ветвях одного и того же репозитория **Git**, будет получена ошибка конфликта слияния при попытке выполнить слияние для этих ветвей. Необходимо разрешить этот конфликт слияния с помощью новой фиксации, прежде чем можно будет выполнить слияние для этих ветвей.

1. Выполните ``git status``

Отображения конфликта выглядит так ``<<<<<<< конфликт >>>>>>>``

2. Решите, хотите ли вы сохранить изменения только в одной ветке, или только в другой ветви или внести совершенно новое изменение, которое может включать изменения в обеих ветвях. Удалите конфликтующие маркеры ``<<<<<<<, =======, >>>>>>>`` и внесите необходимые изменения в окончательном объединении. 

3. Добавьте или внесите свои изменения с помощью команду ``git add``

4. Зафиксируйте изменения с помощью комментария выполнив команду ``git commit -m "Комментарий"``


### Конфликт слияния при удалении и изменения файла

Если вы редактировали файл, такой как **README.md**, а другой человек удалил его же в другой ветви того же репозитория **Git**, вы получите сообщение об ошибке конфликта слияния при попытке выполнить слияние для этих веток. Необходимо разрешить этот конфликт слияния с помощью новой фиксации, прежде чем можно будет выполнить слияние для этих ветвей.

1. Выполните ``git status``

2. Решите, хотите ли сохранить удаленный файл. 

*Чтобы добавить удаленный файл обратно в репозиторий, выполните следующие действия:*

```
git add README.md
```

*Чтобы удалить этот файл из репозитория, выполните следующие действия:*

```
git rm README.md
> README.md: needs merge
> rm 'README.md'
```

3. Зафиксируйте изменения с помощью комментария.

```
git commit -m "Resolve merge conflict by keeping README.md file"
```

или

```
> [branch-d 6f89e49] Merge branch 'branch-c' into branch-d
```

***
[**Содержание**](/readme.md)

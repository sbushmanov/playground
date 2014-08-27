---
title: "Создание новой ветки в RStudio"
author: "Sergey Bushmanov"
date: "08/27/2014"
output: html_document
---


# Header id="top"

1. Создать репозиторий в GitHub
2. Создать проект в RStudio
3. В командной строке в домашней директории проекта:


```r
git branch gh-pages
```

4. Для того, чтобы можно было пользоваться интерфейсом RStudio поменять файл `"./.git/config"` :


```r
[core]
        repositoryformatversion = 0
    filemode = true
    bare = false
    logallrefupdates = true
[remote "origin"]
    url = git@github.com:sbushmanov/gh-play.git
    fetch = +refs/heads/*:refs/remotes/origin/*
[branch "master"]
    remote = origin
    merge = refs/heads/master
# начало добавить
[branch "gh-pages"]
    remote = origin
    merge = refs/heads/gh-pages
# конец добавить
```

6. Создать файл .`nojekyll` в корне рабочей директории :


```r
file.create(".nojekyll")
```

[go to top](#top)

```r
x <- function(x) {
        return(x)
}
```

- [ ] item 1
- [x] item 2

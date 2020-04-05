# Как это работает
## Markdown
Существует язык разметки под названием [Markdown](https://en.wikipedia.org/wiki/Markdown). Синтаксис его довольно простой, по сути это текстовый файл с расширением md. Довольно хорошее [описание Markdown](https://gist.github.com/Jekins/2bf2d0638163f1294637).

## MkDocs
Браузер ни чего не знает про Markdown, но знает про HTML. Нужно как-то преобразовать Markdown в HTML. Существует много решений для этого, но мы остановились на MkDocs.

MkDocs - генератор статических сайтов из Markdown. На [официальном сайте](https://www.mkdocs.org) есть подробная инструкция по его установке локально и генерации им статических сайтов. Данный сайт по ней и был создан.

Минимально MkDocs для генерации сайта нужен конфигурационный файл `mkdocs.yml` и `index.md` в папке `docs`, расположенной рядом с `mkdocs.yml`:
```
user@comp:~/mkdocs/test-docs$ tree
.
├── docs
│   └── index.md
└── mkdocs.yml
```

## Read the Docs

Генерировать сайт через MkDocs можно локально (здесь будет ссылка как это сделать), затем полученные файлы размещать на какой-нибудь хостинг статических сайтов, например [GitHub Pages](https://pages.github.com/). А можно при помощи сервиса [Read the Docs](https://readthedocs.org/).

Для этого нужно конфигурационные файлы (в нашем случае `mkdocs.yml`) и файлы документов в формате Markdown (в нашем случае папку `docs` с `index.md`) разместить в публичном git-репозитории, к примеру в [GitHub](https://github.com/).

Публичный git-репозиторий [подключаем к Read the Docs](https://docs.readthedocs.io/en/stable/intro/import-guide.html) 

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

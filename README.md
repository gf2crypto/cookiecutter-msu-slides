# cookiecutter-msu-slides

Репозиторий содержит `cookiecutter` ([more details](https://cookiecutter.readthedocs.io/en/latest/)) LaTeX-шаблон для оформления презентаций работ студентов (курсовых работ, выпускных квалификационных работ бакалавров, магистерских диссертаций и т.п.).

Шаблон адаптирован для студентов кафедры информационной безопасности факультета вычислительной математики и кибернетики. Однако он имеет достаточно гибкие настройки и может быть сравнительно легко приспособлен для других кафедр, факультетов и университетов.

## Как использовать шаблон
1. Установите `python` и `git`;
2. Установите приложение `cookiecutter`, выполнив в командной строке следующую команду:
   ```bash
   pip install cookiecutter
   ```
4. Для инициализации нового проекта выполните в командной строке:
   ```bash
   cookiecutter https://github.com/gf2crypto/cookiecutter-msu-slides.git
   ```
5. Параметры:
     - **project_name**, имя проекта (поддерживается только латиница);
     - **create_gitignore**, требуется ли создать `.gitignore` файл для использования системы контроля версий `git`: 'yes' или 'no'.
5. Размещайте свои `tex`-файлы внутрь каталог `mainfiles`, включайте новые файлы с помощью директив `\include` или `\input` в главный файл `<project_name>.source.tex`, который расположен также в каталоге `mainfiles`. Файлы рисунков помещайте в каталог `images`. Свои команды можно добавлять в файл `commands`.
6. Для компиляции документа можно использовать команду `make` (`make.bat` под `Windows`).
7. Запустите `make help` (`make.bat help` для `Windows`), чтобы увидеть другие возможные опции компиляции. Рекомендуется обратить внимание на опцию `watch`, которая обеспечивает непрерывную компиляцию проекта и позволяет видеть изменения в `pdf` практически в режиме реального времени.

__ВНИМАНИЕ! `make`-файлы используют `latexmk` для компиляции документа! Рекомендуется устанавливать полную версию `LaTeX`, чтобы сэкономить время на отладке и доустановке пакетов!__

## Установка вручную
В ветке `example` содержится интерполированная версия шаблона. Поэтому, если возникли сложности с установкой `python` или `cookiecutter`, то можно скачать файлы из этой ветки и дальше адаптировать их вручную под конкретный проект.

Скачать ветку можно по ссылке: [zip](https://github.com/gf2crypto/cookiecutter-msu-slides/archive/example.zip) или сначала клонировать репозиторий с помощью команды `git clone https://github.com/gf2crypto/cookiecutter-msu-slides.git`, а потом перейти на ветку `example`, выполнив в папке клонированного репозитория команду `git checkout example`.


Shield: [![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a [Creative Commons Attribution 4.0 International
License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

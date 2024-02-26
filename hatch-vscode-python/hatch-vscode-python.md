---
date: 2023-12-27
categories: [it, programming]
tags: [Python, VScode]
published: false
author: Anton Sergienko
author-email: anton.b.sergienko@gmail.com
license: CC BY 4.0
license-url: https://github.com/Harrix/harrix.dev/blob/main/LICENSE.md
permalink-source: https://github.com/Harrix/harrix.dev-articles-2023/blob/main/hatch-vscode-python/hatch-vscode-python.md
permalink: https://harrix.dev/ru/articles/2023/hatch-vscode-python/
lang: ru
attribution:
  - {
      author: Python Software Foundation,
      author-site: "https://www.python.org/psf/",
      license: GNU General Public License,
      license-url: "https://en.wikipedia.org/wiki/GNU_General_Public_License",
      permalink: "https://commons.wikimedia.org/wiki/File:Python_logo_and_wordmark.svg",
      permalink-date: 2021-08-01,
      name: Python logo and wordmark.svg,
    }
  - {
      author: Microsoft Corporation,
      author-site: "https://www.microsoft.com/",
      license: MIT,
      license-url: "https://github.com/pypa/hatch/blob/master/LICENSE.txt",
      permalink: "https://raw.githubusercontent.com/pypa/hatch/master/docs/assets/images/logo.svg",
      permalink-date: 2024-01-29,
      name: Hatch Logo,
    }
---

# Настройка Hatch (Python) в VSCode

![Featured image](featured-image.svg)

Вместо Pipenv, venv используем современный Hatch для работы с виртуальным окружением.

## Ссылки

- [Hatch](https://hatch.pypa.io/latest/) — документация.

## Подготовка

<details>
<summary>Установка программ и создание папки для проектов</summary>

Разумеется, нужен Python. Если его нет, то смотрите статью [Установка Python](https://github.com/Harrix/harrix.dev-articles-2021/blob/main/install-python/install-python.md) | [🡥](https://harrix.dev/ru/articles/2021/install-python/).

Нужен VSCode. Если его нет, то смотрите статью [Установка Visual Studio Code (простая)](https://github.com/Harrix/harrix.dev-articles-2021/blob/main/install-vscode-simple/install-vscode-simple.md) | [🡥](https://harrix.dev/ru/articles/2021/install-vscode-simple/).

Нужно расширение Python в VScode:

![Установка расширения Python](img/python-extention.png)

_Рисунок 1 — Установка расширения Python_

Не забудьте перейти в раздел файлов:

![Раздел Explorer](img/explorer.png)

_Рисунок 2 — Раздел Explorer_

Создайте на компьютере папку, где будут располагаться проекты, например, `C:\python-projects`, если у вас еще нет папки для Python проектов (например, через команду `mkdir C:\python_projects\` или просто через проводник). Через `File` → `Open Folder...` откройте эту папку (там тоже через окно открытия папки можно создать нужную папку):

![Открытие папки](img/open-folder_01.png)

_Рисунок 3 — Открытие папки_

Вас спросят о том, доверяете ли вы авторам этой папки. Но ведь эту папку вы только что создали? Так что доверяем:

![Подтверждение доступа к папке](img/open-folder_02.png)

_Рисунок 4 — Подтверждение доступа к папке_

И включите режим автосохранения, чтобы не забывать сохранять изменения в файле:

![Режим Auto Save](img/auto-save.png)

_Рисунок 5 — Режим Auto Save_

</details>

## Краткий пересказ

```console
pip install hatch
mkdir C:\python_projects\
cd C:\python_projects\
hatch new "Test Hatch"
cd test-hatch
hatch shell
```

## Установка Hatch и создание проекта

Вызываем консоль `Ctrl` → `` ` `` (`Ctrl` → `Ё`), прописываем команду установки Hatch глобально (после ввода команды не забываем нажать `Enter`):

```console
pip install hatch
```

![Установка Hatch](img/install.png)

_Рисунок 6 — Установка Hatch_

Если команда не срабатывает, то попробуйте `python -m pip install hatch`.

Возможно, что вас попросят обновить `pip` через команду `python.exe -m pip install --upgrade pip`. Почему бы и нет (скриншот приведен из другого эксперимента с Hatch):

![Обновление pip](img/update-pip.png)

_Рисунок 7 — Обновление pip_

Теперь можно создать проект для Hatch. Вместо `Test Hatch` введите имя своего проекта:

```console
hatch new "Test Hatch"
```

![Инициализация проекта](img/init_01.png)

_Рисунок 8 — Инициализация проекта_

Итак, у нас из названия проекта `Test Hatch` создалась папка `test-hatch`. Если вы назвали проект по другому, то и название папки будет другим. Командой `cd test-hatch` переходим в эту папку проекта:

![Переход в папку проекта](img/init_02.png)

_Рисунок 9 — Переход в папку проекта_

![](img/project.png)

_Рисунок 10 — _

## Виртуальное окружение

Теперь нужно создать виртуальное окружение через команду:

```console
hatch shell
```

![](img/environment_01.png)

_Рисунок 11 — _

![](img/fix_01.png)

_Рисунок 12 — _

![](img/fix_02.png)

_Рисунок 13 — _

![](img/new_file_01.png)

_Рисунок 14 — _

![](img/new_file_02.png)

_Рисунок 15 — _

![](img/environment_02.png)

_Рисунок 16 — _

![](img/environment_03.png)

_Рисунок 17 — _

![](img/environment_04.png)

_Рисунок 18 — _

![](img/environment_05.png)

_Рисунок 19 — _

![](img/environment_06.png)

_Рисунок 20 — _

## Добавление библиотеки

![](img/dependencies_01.png)

_Рисунок 21 — _

![](img/dependencies_03.png)

_Рисунок 22 — _

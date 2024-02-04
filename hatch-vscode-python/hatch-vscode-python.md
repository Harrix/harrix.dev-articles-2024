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

Вместо Pipenv, venv используем современный [Hatch](https://hatch.pypa.io/latest/) для работы с виртуальным окружением.

## Подготовка

<details>
<summary>Установка программ и создание проекта</summary>

Разумеется, нужен Python. Если его нет, то смотрите статью [Установка Python](https://github.com/Harrix/harrix.dev-articles-2021/blob/main/install-python/install-python.md)<!-- https://harrix.dev/ru/articles/2021/install-python/ -->.

Нужен VSCode. Если его нет, то смотрите статью [Установка Visual Studio Code (простая)](https://github.com/Harrix/harrix.dev-articles-2021/blob/main/install-vscode-simple/install-vscode-simple.md)<!-- https://harrix.dev/ru/articles/2021/install-vscode-simple/ -->.

Нужно расширение Python в VScode:

![Установка расширения Python](img/python-extention.png)

_Рисунок 1 — Установка расширения Python_

Не забудьте перейти в раздел файлов:

![Раздел Explorer](img/files.png)

_Рисунок 2 — Раздел Explorer_

Создайте на компьютере папку, где будет располагаться  проект, например, `C:\Projects\test-hatch`.  Через `File` → `Open Folder...` откройте эту папку:

![Открытие папки](img/open-folder_01.png)

_Рисунок 3 — Открытие папки_

Вас спросят о том, доверяете ли вы авторам этой папки. Но ведь эту папку вы только что создали? Так что доверяем:

![Подтверждение доступа к папке](img/open-folder_02.png)

_Рисунок 4 — Подтверждение доступа к папке_

Создаем новый файл в папке, кликая правой кнопкой по пустому пространству в папке:

![Создание нового файла](img/new-file_01.png)

_Рисунок 5 — Создание нового файла_

Вводите имя файл, например, `main.py` и нажимаем `Enter`:

![Ввод имени нового файла](img/new-file_02.png)

_Рисунок 6 — Ввод имени нового файла_

</details>

## Установка Hatch

Вызываем консоль `Ctrl` → `` ` `` (`Ctrl` → `Ё`), прописываем команду установки Hatch глобально:

```console
pip install hatch
```

![Установка Hatch](img/install.png)

_Рисунок 7 — Установка Hatch_

Если команда не срабатывает, то попробуйте `python -m pip install hatch`.

Возможно, что вас попросят обновить `pip` через команду `python.exe -m pip install --upgrade pip`. Почему бы и нет:

![Обновление pip](img/update-pip.png)

_Рисунок 8 — Обновление pip_

Теперь можно инициализировать рфеср с виртуальной средой через команду:

```console
hatch  install hatch
```

![](img/init.png)

_Рисунок  — _

![](img/.png)

_Рисунок  — _

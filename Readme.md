# О шаблоне
Этот шаблон для VScode или Overleaf.com. Однако в Overleaf есть бесплатный лимит на время сборки(примерно в 65 страниц).


# Начало работы Overleaf

- Скачать репозиторий в zip файле

- Зайти на Overleaf.com

    - Нажать New Project -> Upload Project -> выбрать zip-файл

# Начало работы VScode 

- Скачать [latex](https://www.tug.org/texlive/acquire-netinstall.html)
    - Для Windows -  install-tl-windows.exe

- Для VScode установить плагин [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

- Перейти C:\Users\%USER%\AppData\Roaming\Code\User\settings.json
    - измените основной файл строками из шаблонного [settings.json](settings.json)
- Откройте в VScode папку с шаблоном
    - должен подгрузится плагин LaTeX Workshop
- В настройке LaTeX Workshop выберите рецепт сборки "pdflatex -> bibtex -> pdflatex * 2" или latexmk
- Перейдите в [document/documentMain.tex](document/documentMain.tex) и запустите сборку

# Структура

- Для работы нужны папки:
    - папка document - тут находится файлы вашего документа.
    - папка Source - сюда ложите картинки, файлы для листинга и тп.
    - папка main - тут находятся стиливые файлы и будут находится выходные PDF-файлы.
- папка document содержит:
    - [preamble.tex](document/preamble.tex) - настройка документа( зайдите почитайте, там все подписано)
    - [title-page-preamble.tex](document/title-page-preamble.tex) - заполнение полей для вставки титульной страницы
    - [documentMain.tex](document/documentMain.tex) - файл с вашим текстом. Текст можно писать непосредственно в этом файле или разделять на отдельные главы, а после импортировать.
    - chapter/ - необязательная папка с главами документа.  
    - [documentAppendixProgram.tex](document/documentAppendixProgram.tex) - файл приложения текста программы.    
    - [biblio/biblio_src.bib](document/biblio/biblio_src.bib) - список источников. Примеры заполнения можно посмотреть в [docs/ugost2008.pdf](docs/ugost2008.pdf).
- папка Source содержит:
    - папка img - сюда можно помещать картинки для в ставки в документ. Если картинка находится в этой папке, то указание полного пути вставки не обязательно, можно указать только название.
    - папка background  - сюда можно помещать фоны рамок.

# Полезности

Быстрый переход от PDF к .tex: 
 - для VScode: наведите указатель мыши в просмоторщике PDF-файла на слово, а после зажмите `Ctrl` и кликните ЛКМ на слово. Откроется .tex файл, где было это слово написано, а указатель будет в соответсвующем месте. 
 - для Overleaf: на границе текстового редактора и окна просмотра  PDF-файла находятся кнопки в виде стрелок имеющие аналогичные функции.



# Инструкция для работы с Git и удалёнными репозиториями

## Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.

## Подготовка репозитория
Для создание репозитория необходимо выполнить команду *git init* в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

## Создание коммитов

### Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду *git add* напишите *git add <имя файла>*

### Просмотр состояния репозитория
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

### Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

## Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с репозиторием следующим образом: *git checkout <номер коммита>*

## <u>Просмотр истории версий</u>

Вывод на экран журнала истории версий файла с коммитами и их хеш-кодами.  Базовым и самым мощным инструментом в данном случае является команда *git log*.

## <u>Просмотр разницы между текущим и закоммиченным файлом </u>

Команда *git diff* без дополнительных параметров позволяет посмотреть, что было изменено, но пока не проиндексировано.
Эта команда сравнивает содержимое в рабочей папке и в области индексирования. Она выводит список изменений, которые вы внесли, но пока не проиндек¬сировали.
Важно помнить, что сама по себе команда *git diff* показывает не все изменения, сделанные с момента последней фиксации состояния, а только те, которые еще не проиндексированы. То есть если вы проиндексировали все сделанные изменения, команда *git diff* ничего вам не вернет.

## <u> Удаление файлов </u>

Чтобы система Git перестала работать с файлом, его нужно удалить из числа отслеживаемых (точнее, убрать из области индексирования) и зафиксировать данное изменение. Это делает команда *git rm*, которая заодно удаляет указанный файл из рабочей папки, благодаря чему он исчезает из списка неотслеживаемых.

## <u> Переименование файлов </u>

В Git есть команда *git mv*. Для переименования файла можно написать:
*$ git mv file_from file_to*

## <u> Отмена изменений </u>
Необходимость отмены внесенных изменений может возникнуть на любой стадии проекта. **Однако здесь следует быть крайне осторожным, ведь после отмены далеко не всегда существует возможность вернуться в предшествующее состояние.** <u>Это одна из немногих ситуаций при работе с Git, когда неверные действия могут привести к потере результатов вашего труда.</u>
Необходимость отмены чаще всего возникает при слишком ранней фиксации из¬менений, когда вы забыли добавить в коммит какие-то файлы или ошиблись с со¬общением фиксации. Для повторного сохранения версии в такой ситуации можно воспользоваться параметром <u> --amend</u> :

*$ git commit –amend*

## <u> Ветки в Git </u>

### Создание ветки

Для создания новой ветки в Git существует команда *git branch.* Например, *__git branch имя новой ветки__*.

### Переход между ветками

Чтобы перейти между ветками, нужно использовать команду *git checkout*. Например, *__git checkout имя ветки__*.

### Слияние ветки

Для того, чтобы слить ветки используем команду *git merge*. 

**Во-первых, нужно перейти в ту ветку, в которую мы хотим добавить.**

Затем набрать команду *__git merge имя ветки__*, из которой сливаем информацию.  

### Удаление ветки

Когда ветка нам уже не нужна, ее можно удалить. Это делается командой **git branch -d имя ветки**.

### Управление ветками

Теперь, когда вы знаете, как создаются, сливаются и удаляются ветки, рассмотрим другие инструменты, которые пригодятся при постоянной работе с ветками.
Команда  *__git branch__*  позволяет не только создавать и удалять ветки. Запущенная без аргументов, она выводит на экран список имеющихся веток.









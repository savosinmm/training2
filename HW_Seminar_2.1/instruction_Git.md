# Инструкция по основным командам Git

## Что такое Git и зачем он нужен?

**Git** - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. Например, для картинок - полезно для дизайнеров.

## Репозиторий 
**это хранилище файлов, поддерживающее версионность**

 * *Команда создающая репозиторий*

**git init**

## Версионность файла

* *Команда добавляющая файлу версионность в локальном репозитории*

**git add**

## Фиксация изменений в файле

* *Команда фиксирующая изменения и сообщающая о появлении новых версий файл*

**git commit**

## Разница между текущей версией файла и зафиксированной

* *Команда показывает разницу между текущей и уже зафиксированной версией файла*

**git diff**

## Информация о всех коммитах
* *Команда выводит список всех коммитов (сохранений) в хронологическом порядке*

**git log**

## Перемещение между сохранениями
* *Команда позволяет перемещаться между сохранениями*

**git checkout**

##Подсказки по популярным командам:

# По популярным командам
* *Выдает список популярных команд*
**git help**

*Или по конкретной команде*
* *Выдает описание по понкретной команде*
**git help <название_команды>**

*Например clone*
* *git help clone*

# Работа с удаленными репозиториями
* *Скачивание из текущего репозитория и слияние со своей версией* 

**git clone** команда для копирования внешнего репозитория на свой ПК 

![Пример](opisanie.jpg)

Команда git clone составная: она не только
загружает все изменения, но и пытается слить
все ветки на локальном компьютере и в
удаленном репозитории.

**git pull** авторизация.

Эта команда позволяет скачать все
из текущего репозитория и автоматически
сделать merge с нашей версией

![Пример](pull.jpg)

**git push**

Эта команда позволяет отправить нашу
версию репозитория на внешний
репозиторий. ТРЕБУЕТ АВТОРИЗАЦИИ
на внешнем репозитории.

![Пример](push.jpg)


# Как настроить совместную работу

1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. “Подружить” ваш локальный и удалённый репозитории. 

 *GitHub при создании нового репозитория подскажет, как это можно сделать*

4. Отправить (push) ваш локальный репозиторий в удалённый (на GitHub), при этом, возможно, вам нужно будет авторизоваться на удалённом репозитории
5. Провести изменения “с другого компьютера”
6. Выкачать (pull) актуальное состояние из удалённого репозитория

# Отключение удаленного репозитория от локального   
Иногда возникает необходимость забыть удаленный репозиторий. Для этого существует команда **git remote remove**
**Формат**
git remote remove <название удаленного репозитория>
**Пример**
# Отключим удаленный репозиторий с именем origin
$ git remote remove origin

Данная команда предельно проста в использовании. В качестве имени репозитория нужно передавать то имя, которое вы указывали в команде git remote add. Заметьте, данная команда не удаляет удаленный репозиторий с сервера, она удаляет только подключение вашего репозитория к удаленному.

# Инструкция для работы с Git и удалёнными репозиториями
# Что такое Git?
Git - это одна из реализаций распределённых систем контроля версий, имеющая как и локальные, так и удалённые репозитории. Является самой популярной реализацией систем контроля версий в мире.
# Подготовка репозитория
Для создание репозитория необходимо выполнить команду _git init_ в папке с репозиторием и у Вас создаться репозиторий (появится скрытая папка .git)

# Создание коммитов
## Git add
Для добавления измений в коммит используется команда *git add*. Чтобы использовать команду git add напишите *git add <имя файла>*

Просмотр состояния репозитория
---
Для того, чтобы посмотреть состояние репозитория используется команда *git status*. Для этого необходимо в папке с репозиторием написать *git status*, и Вы увидите были ли измения в файлах, или их не было.

## Создание коммитов
Для того, чтобы создать коммит(сохранение) необходимо выполнить команду *git commit*. Выполняется она так: *git commit -m "<сообщение к коммиту>*. Все файлы для коммита должны быть ***ДОБАВЛЕНЫ*** и сообщение к коммиту писать ***ОБЯЗАТЕЛЬНО***.

# Добавление картинок
## Картинка
   ![картинки](https://miro.medium.com/max/1400/1*vlDY5078rLn0dFQWbdAKUA.png)
## Гифка
   ![гиф](https://raw.githubusercontent.com/nadehi18/battery-wallpaper-windows/master/preview/charging.gif)
## Картинка из папки
   ![картинка](1_S-_fv45WT4MgqtnPVsxtHQ.jpeg)

# Перемещение между сохранениями
Для того, чтобы перемещаться между коммитами, используется команда *git checkout*. Используется она в папке с пепозиторием следующим образом: *git checkout <номер коммита>*
# Слияние веток
Для того чтобы дабавить ветку в текущую ветку используется команда *git merge*
# Журнал изменений
Для того, чтобы посмтреть все сделанные изменения в репозитории, используется команда _git log_. Для этого достаточно выполнить команду _git log_ в папке с репозиторием
# Ветки в Git
Создание ветки
Для того, чтобы создать ветку, используется команда *git branch*. Делается это следующим образом в папке с репозиторием: *git branch <название новой ветки>*

смотрим команду git commit -am "save all"

<br></p>
# Работа с удаленными репозиториями

## Установка удаленного репо на локал

Для установки удаленного репо на локальную машине, нам потребуется команда ***git cone*** <ссылка на удаленный репозиторий>. Если репо пренадлежит не вам, вы не смодете вносить изменения в удаленный репо и предлагать правки.

Если вы решили комуто помочьс проектом, то для начала у вас должна быть учетная запись хабе репозитариев, например таком как GitHub. После этого, вы делаете "Fork" удаленного репо. Создается его актуализированная копия на вашей учетке. Далее, на локальной машине, вы делаете команду ***git cone*** <ссылка на fork>. После, вам необходимо создать свою ветку и в ней уже делать изменения.

Команда ***git pull*** обновит ваш локальный репо, до состояния удаленного, нужно помнить, что она мержит содержимое.

Команда ***git push*** используется для выгрузки содержимого локального репозитория в удаленный репозиторий. Она позволяет передать коммиты из локального репозитория в удаленный. Эта команда симметрична команде git fetch: при извлечении с помощью fetch коммиты импортируются в локальные ветки, а при публикации с помощью push коммиты экспортируются в удаленные ветки.

Команда ***пit fetch*** используется для скачивания изменений из удаленного или локального репозитория в свой локальный репозиторий. Польза git fetch в том, что эта команда привносит актуальность локальному репозиторию без изменения его дерева или текущей ветки.

Команда pull автоматически сливает коммиты, не давая вам сначала просмотреть их. Если вы не пристально следите за ветками, выполнение этой команды может привести к частым конфликтам.
При использовании fetch, git собирает все коммиты из целевой ветки, которых нет в текущей ветке, и сохраняет их в локальном репозитории. Однако он не сливает их в текущую ветку.

Команда ***git remote*** позволит узнать, с каким удаленным репо вы работаете. Для вывода большей информации используется флаг "-v". Таким образом ***git remote -v*** . Так же можно использовать ***git remote show <remote>***

Команда ***git remote rename*** позволяет переименовать удаленный репо.
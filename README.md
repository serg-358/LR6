# Отчёт о лабораторной работе №6

**Цель лаборатной работы**: изучение базовых возможностей системы управления версиями, опыт работы с Git Api, опыт работы с локальным и удалённым репозиторием.

**Ход работы**:

Шаги 1, 3 и 4 были выполнены ранее.

Шаг 2: Сделать копию в личное хранилище. 
Для этого в интерфейсе GitHub сделан форк исходного репозитория (рис. 1).

![Рис. 1](https://github.com/serg-358/LR6/blob/report/Скриншоты/001.png)

Рис. 1 - Форк исходного репозитория

Шаг 5: Клонирование личного удалённого репозитория на компьютер (рис. 2).

![Рис. 2](https://github.com/serg-358/LR6/blob/report/Скриншоты/002.png)

Рис. 2 - Клонирование репозитория

Шаг 6: Добавить файл через интерфейс GitHub и подтянуть изменения.
Добавлен файл график.py с программой для построения графика (рис. 3).

![Рис. 3](https://github.com/serg-358/LR6/blob/report/Скриншоты/003.png)

Рис. 3 - Обновление изменений в репозитории на компьютере

Шаг 7: Получить историю операций для каждой из веток (рис. 4-6).

![Рис. 4](https://github.com/serg-358/LR6/blob/report/Скриншоты/004.png)

Рис. 4 - Подключение ветки branch1

![Рис. 5](https://github.com/serg-358/LR6/blob/report/Скриншоты/005.png)

Рис. 5 - История операций в ветке branch1

![Рис. 6](https://github.com/serg-358/LR6/blob/report/Скриншоты/006.png)

Рис. 6 - История операций в ветке master

Шаг 8: Просмотреть последние изменения (рис. 7-8).

![Рис. 7](https://github.com/serg-358/LR6/blob/report/Скриншоты/007.png)

Рис. 7 - Последние изменения в ветке branch1

![Рис. 8](https://github.com/serg-358/LR6/blob/report/Скриншоты/008.png)

Рис. 8 - Последние изменения в ветке master

Шаг 9: Выполнить слияние в ветку master, разрешив конфликт (рис. 9-13).

![Рис. 9](https://github.com/serg-358/LR6/blob/report/Скриншоты/009.png)

Рис. 9 - Различия между ветками

![Рис. 10](https://github.com/serg-358/LR6/blob/report/Скриншоты/010.png)

Рис. 10 - Попытка слияния с конфликтом

![Рис. 11](https://github.com/serg-358/LR6/blob/report/Скриншоты/011.png)

Рис. 11 - Файл mergefile.txt до изменений

![Рис. 12](https://github.com/serg-358/LR6/blob/report/Скриншоты/012.png)

Рис. 12 - Файл mergefile.txt после изменений

![Рис. 13](https://github.com/serg-358/LR6/blob/report/Скриншоты/013.png)

Рис. 13 - Слияние веток

Шаг 10: Удалить побочную ветку после слияния (рис. 14).

![Рис. 14](https://github.com/serg-358/LR6/blob/report/Скриншоты/014.png)

Рис. 14 - Удаление ветки с проверкой

Шаг 11: Сделать изменения в файле с фиксацией (рис. 15).

![Рис. 15](https://github.com/serg-358/LR6/blob/report/Скриншоты/015.png)

Рис. 15 - Коммиты изменений в файле график.py

Шаг 12: Сделать откат коммита (рис. 16-17).
Команда для просмотра последних 5 изменений - `git log --oneline -5`.

![Рис. 16](https://github.com/serg-358/LR6/blob/report/Скриншоты/016.png)

Рис. 16 - Последние 5 изменений

Для отката коммита применяется команда `git revert 413a960`, где 413a960 - хэш нужного коммита.

![Рис. 17](https://github.com/serg-358/LR6/blob/report/Скриншоты/017.png)

Рис. 17 - Публикация отката коммита

Откат коммита в репозитории обозначен как "Текущие изменения".

Шаг 13: Создать ветку для отчёта (рис. 18).

![Рис. 18](https://github.com/serg-358/LR6/blob/report/Скриншоты/018.png)

Рис. 18 - Создание ветки и папки для скринов

Шаг 14: Отчёт в файле README.md

![Рис. 19](https://github.com/serg-358/LR6/blob/report/Скриншоты/019.png)

Рис. 19 - Добавление скринов в папку

![Рис. 20](https://github.com/serg-358/LR6/blob/report/Скриншоты/020.png)

Рис. 20 - Коммит изменений в папке

Лог команд в Git Bash:

-`git clone https://github.com/serg-358/LR6.git`
-`cd LR6`
-`git pull origin master`
-`git fetch upstream`
-`git checkout -b branch1 upstream/branch1`
-`git push origin branch1`
-`git checkout master`
-`git log origin/branch1`
-`git log origin/master`
-`git checkout branch1`
-`git log --oneline`
-`git show`
-`git checkout master`
-`git log --oneline`
-`git show`
-`git diff master..branch1`
-`git merge branch1`
-`git status`
-`nano mergefile.txt`
-`git add mergefile.txt`
-`git commit -m "Разрешение конфликта, слияние веток"`
-`git merge branch1`
-`git branch -d branch1`
-`git branch`
-`nano график.py`
-`git add график.py`
-`git commit -m "Внесено первое изменение в файл"`
-`nano график.py`
-`git add график.py`
-`git commit -m "Внесено второе изменение в файл"`
-`git log --oneline -5`
-`git revert 413a960`
-`git status`
-`git push origin master`
-`git commit -m "Текущие изменения"`
-`git checkout -b report`
-`mrdir Скриншоты`
-`ls`
-`git push origin report`
-`git status`
-`git add Скриншоты/`
-`git status`
-`git commit -m "Скриншоты добавлены в отдельную папку"`
-`git push origin report`
-`git add Скриншоты/`
-`git commit -m "Добавлены два скрина"`
-`git pull origin report`
-`git push origin report`
-`git log --pretty=format:"%h %ad %an: %s" --date=short -30`
-`git add Скриншоты/`
-`git commit -m "История операций в форматированном виде"`
-`git pull origin report`
-`git push origin report`

Шаг 15: Получить историю операций в форматированном виде (рис. 21)

![Рис. 21](https://github.com/serg-358/LR6/blob/report/Скриншоты/021.png)

Рис. 21 - История операций в форматированном виде

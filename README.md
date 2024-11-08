# Мое изучение Git

### Подготовка

||Комманда в **bach**|
|-|-|
|Настройка имени:|git config --global user.name "..."|
|Настройка email:|git config --global user.email "..."|
|Настройка ветки по умолчанию:|git config --global init.defaultBranch main|
|Корректная обработка окончаний строк:|git config --global core.autocrlf true    git config --global core.safecrlf warn|

### Создание репозитория

||Комманда в **bach**|
|-|-|
|Инициация локального репозитория:|git init|
|Проверка является ли репозиторий удаленным:|git remote -v|
|Связь  локального репозитория с удаленным:|git remote add origin ссылка на репозиторий|
|Добавление еще одного уделенного репозитория к локальному:|git remote add target ссылка-на-репозиторий|
|Удаление текущей связи локального репозитория с удаленным:|git remote rm origin|

### Работа с локальным репозиторием

||Комманда в **bach**|
|-|-|
|Статус репозитория:|git status|
|Добавление файла в отслеживаемые:|git add имя файла (git add -A  - добавляет все неотслеживаемы файлы):|
|Удаление файла или папки из отслеживаемых:|git rm --cached имя-файла|
|Создание файла-настройки, который позволяет игнорировать нужные папки и файлы во время публикации в удалённый репозиторий:|.gitignore|
|Сохранение коммита:|git commit -m "Initial commit"|
|Объединие комманд git add и git commit:|git commit -a -m "..."|
|Добавление файла в последний коммит:|git commit --amend -m “...”|
|Создание нового коммита, в котором отменен коммит с последними изменениями:|git revert хеш|
|Переключение между коммитам:|git checkout хеш|
|Возвращение на последний коммит:|git checkout -|

### Ветки 

||Комманда в **bach**|
|-|-|
|Просмотр веток в репозитории:|git branch|
|Создание новой ветки и переход на нее|git checkout -b имя-новой-ветки|
|Объединение двух веток:|git merge название ветки|

### Передача данных на удаленный репозиторий 

||Комманда в **bach**|
|-|-|
|Сохранение в основной ветке main:|git push -u origin main|
|Сохранение в дополнительной ветке:|git push -u origin new-text|
|Сохранение основной ветки в дополнительном репозитории:|git push -u target main|

### Совместная работа

||Комманда в **bach**|
|-|-|
|Клонирование репозитория, клонируется только ветка  main:|git clone ссылка-на-репозиторий|
|Просмотр других веток, которые есть в клонированном репозитории:|git branch -a|
|Скачивание изменений из удаленного репозитория:|git pull|
|Скачивает изменения из удалённого репозитория и сохраняет их в промежуточном состоянии, не применяя к файлам на компьютере:|git fetch|
|Открывает историю репозитория:|git log --oneline|
|Открывает всю историю репозитория:|git log --oneline -- all|

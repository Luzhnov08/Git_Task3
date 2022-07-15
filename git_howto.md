#Инструкция пользователя git

##Основные команды и настройки

*git config --local <<< git config --global <<< git config --system 
>приоритет настроек по возрастанию
*git config --list 
>список всех настроек
*git config --global core.editor "'C:\Program Files (x86)\Notepad++\notepad++.exe' -multiInst -notabbar -nosession -noPlugin" 
>заменить редактор текста на notepad
*git init 
>инициализация репозитория
*tree.git 
>просмотр дерева файлов и папок
*файлы: 1)Unmodified, modified, staged 2)Untracked
*файлы в основном, в состоянии: modified, staged, commited

*git add <File_name> отслеживать файл
*git commit 
>фиксация изменений
*git status 
>состояние файлов
*git diff 
>Различия файлов
*git log 
>история изменений
*git checkout --<folder/File> (отмена изменений)
*git mv <File Folder>/ 
>перемещение файла
*git reset --hard HEAD 
>жесткий сброс 
*git reset HEAD <folder/File> 
>убрать из индекса
*git branch testing 
>создать новую ветку
*clear 
>очистить окно терминала
*git cat-file -t <Hash-code> 
>проверить тип файла ключ -p содержимое

##Слияние

*git commit -a -m "Commit_Text"
*git merge *Branch Name* 
>перед этим перейти на мастер-ветку
*git reset --merge 
>устранить конфликт
*если устранить конфликт вручную в файле, то нужно в git выполнить:* add <FileName>

##Метки
*аннотированные/неаннотированные*
*git tag 
>команда на просмотр метки, легковесная метка
*git show *tagName* >просмотр указателей
*Пример:* git tag -a v.1.0 -m "Version 1.0" *аннотированная метка*

##Удалённые репозитории: bitbucket, github

*git remote -v 
>список источников
*git remote add bitbucket http:// 
>добавить источник
*git push bitbucket 
>загрузить изменения на сервер
*git push --set-upstream bitbucket master 
>указать источник
*git push --tags bitbucket 
>добавить все метки в репозит
*git fetch 
>список изменений с сервера
*git pull 
>получить изменения

#Модели ветвления: Git Flow / GitHub flow / Gitlab flow

*Git Flow: 
>подходит Scrum, Waterfall главные ветки: master, develop Вспом.: feature, release, hotfix
*Github Flow: 
>подходит Scrum, Waterfall главные ветки: master Вспом.: feature, hotfix (для скриптов развертывания)
*Gitlab Flow: 
>главные ветки: master Вспом.: feature, hotfix стабильная ветка: production, необяз. Pre-production
*Краткая инструкция последовательности действий:*
1. Create a branch 
2. Pull-request 
3. Merge the Branch

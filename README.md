# Помощник в создание файлов и переноса в GitHub

## Работа с консолью

На MacBook вы можете открыть *Терминал*
При открытие у тебя будет указана твоя текущая и основная директория **ИМЯ@MacBook-Air-ИМЯ ~ %**

Консольная навигация: **ls** (отобразить содержимое директории) и **cd** (сменить директорию)

Можно проверить какие папки есть в основной директории:

ИМЯ@MacBook-Air-ИМЯ % ls

### Создание файлов и директорий

touch %ИМЯ_ФАЙЛА% или mkdir %ИМЯ_ДИРЕКТОРИИ%

ИМЯ@MacBook-Air-ИМЯ % ls

ИМЯ@MacBook-Air-ИМЯ % cd Documents

ИМЯ@MacBook-Air-ИМЯ documents % mkdir project


### Создать удаленный депозиторий на GitHub


Зайти в свой профиль на GitHub. Далее выбрать *Repositories* --> *New*.
Задаем имя репозиторию *project*. 


Теперь необходимо соединить его с нашей папкой. 
Откройте консоль, перейдите в каталог локального репозитория и введите команду git remote add

ИМЯ@MacBook-Air-ИМЯ project % git remote add origin git@github.com:ИМЯ/assistant-project.git

ИМЯ@MacBook-Air-ИМЯ project % git remote -v

Должно появится две строчки:

origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (fetch)

origin    git@github.com:%ИМЯ_АККАУНТА%/%ИМЯ-ПРОЕКТА%.git (push) 


### Инициализировать Git


ИМЯ@MacBook-Air-ИМЯ project % git init

Получаем такое сообщение: *Initialized empty Git repository in /Users/ИМЯ/Documents/assistant-project/.git/*

Далее необходимо создать файл внутри репозитория


ИМЯ@MacBook-Air-ИМЯ project % touch Text.txt

ИМЯ@MacBook-Air-ИМЯ project % ls

*И проверить статус:*

ИМЯ@MacBook-Air-ИМЯ project % git status

Получаем такое сообщение: _No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	Text.txt

nothing added to commit but untracked files present (use "git add" to track)_

### Необходимо добавить файл в комит и передать его в GitHub


ИМЯ@MacBook-Air-ИМЯ project % git add --all

ИМЯ@MacBook-Air-ИМЯ project % git status


#### При проверке статуса наш файл приобрел зеленый цвет. Далее его необходимо закомитить и передать его в GitHub


ИМЯ@MacBook-Air-ИМЯ project % git commit -m 'Обучение'

ИМЯ@MacBook-Air-ИМЯ project % git push --set-upstream origin main 

(при первом пуше в GitHub. Далее можно будет просто указывать git push)



### Проверить в GitHub что появился наш комит


Обновить страничку в личном кабинете и появится наш проект и наш комит.

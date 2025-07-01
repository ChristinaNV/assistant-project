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


### Инициализировать Git


ИМЯ@MacBook-Air-ИМЯ project % git init

Получаем такое сообщение: *Initialized empty Git repository in /Users/ИМЯ/Documents/assistant-project/.git/*

Далее необходимо создать файл внутри репозитория


ИМЯ@MacBook-Air-ИМЯ project % touch Text.txt
ИМЯ@MacBook-Air-ИМЯ project % ls

И проверить статус:

ИМЯ@MacBook-Air-ИМЯ project % git status

Получаем такое сообщение: *No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
	Text.txt

nothing added to commit but untracked files present (use "git add" to track)*

### Необходимо добавить файл в комит и передать его в GitHub

ИМЯ@MacBook-Air-ИМЯ project % git status
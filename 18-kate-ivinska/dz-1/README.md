# Git - основні команди

### Git — розподілена система керування версіями файлів та спільної роботи.

### Перед початком роботи необхідно [зареєструватись](https://github.com) та скачати застосунок [Git Bash](https://git-scm.com/downloads) за посиланням.

### На початку роботи необхідно проініціалізувати користувача, для цього вказуємо своє ім'я та поштову адресу:
## git config -- global user.name "your name"
*"your name" - ім'я користувача*

## git config -- global user.email "your@ex.com"
*"your@ex.com" - поштова адреса користувача*

### Створення Git-репозиторію.
### Репозиторій - робоча директорія з вашим проектом.

### Коли репозиторій вже створений на сервері, то для того, щоб додати його на свій комп'ютер та працювати з ним необхідно прописати в Git Bash:
## git clone [url]
*[url] - посилання на репозиторій*

### Команда, яка ініціалізує Git як робочу сутність:
## git init

### Щоб почати роботу з проектом, необхідно опинитись в його директорії:
## cd project
*project - назва проекту*

### Щоб закінчити роботу з проектом, необхідно вийти з його директорії:
## cd ..

### По замовчуванню наш проект знаходиться на гілці master. Для того, щоб уникнути конфліктів на сервері необхідно створювати нову гілку для власного проекту.

### Для того, щоб дізнатись а якій гілці ми працюємо:
## git branch

### Щоб створити нову гілку:
## git checkout -b name-branch
*name-branch - назва нової гілки*

### Щоб видалити гілку:
## git checkout -d name-branch
*name-branch - назва гілки*

### Для того, щоб переключитись в основну гілку master
## git checkout master

### Якщо в назві гілки допущено помилку, то її можна виправити:
## git branch -m name-branch1 name-branch2
*name-branch1 - неправильна назва гілки*

*name-branch2 - правильна назва гілки*

### Для того, щоб перевірити стан змінених файлів у нашому проекті(наприклад, README.md), прописуємо команду:
## git status

### Якщо наші файли не були додані, то прописуємо команду:
## git add .

### Після цього знову прописуємо команду git status.

### Для відміни змін, прописуємо команду:
## git reset

### Для видалення файлів з робочої директорії:
## git rm

### Для видалення зайвого сміття з робочої директорії:
## git clean

### Для того, щоб зафіксувати всі збережені зміни та дати їм назву, їх необхідно закомітити:
## git commit -m "message"
*"message" - текстове повідомлення про внесені зміни(наприклад "Create README.md")*

### Щоб відправити свої зміни в репозиторій на GitHub зі свого комп'ютеру необхідно прописати команду:
## git push

### Для імпорту оновлень з серверу GitHub на свій комп'ютер, необхідно прописати:
## git pull

### Для перегляду оновлень на сервері без імпорту на свій комп'ютер:
## git fetch

### Коли зміни однієї гілки заливаєш в іншу гілку, то використовується команда:
## git merge

### Для перегляду всіх оновлень на сервері:
## git fetch --all

### Для видалення гілок, які вже не використовуються в репозиторії:
## git fetch --prune

### Для стягнення змін з головної гілки master в свою:
## git pull origin/master

### Щоб додати до репозиторію всі змінені файли:
## git add -a

### Для того, щоб змінити останній коміт:
## git commit -amend

### Для перепису змін на сервері своїми змінами:
## git push -f

### Для відміни змін у файлі file.js:
## git checkout --app/file.js
*app/file.js - розташування файлу*

### Для відміни змін файлу file.js в гілці master:
## git checkout origin/master

### Для видалення даних на один коміт назад:
## git reset --hard HEAD~1
*HEAD~1 - вказівник на поточну гілку, яка в свою чергу є вказівником на останній коміт в цій гілці*

### Для відновлення будь-яких незафіксованих змін до злиття гілок:
## git merge --abort

### Для копіювання всіх змін конкретного коміту і самого коміту:
## git cherry-pick abccbad
*abccbad - номер коміту*

### Для того, щоб зберегти(сховати) незавершені зміни до окремого контейнеру:
## git stash

### Для перегляду контенерів з незавершеними змінами:
## git stash list

### Для застосування змін з контейнеру з індексом {2}:
## git stash apply stash@{2}

### Для видалення всіх контейнерів зі змінами:
## git stash drop

### Для видалення контейнеру з індексом {2}:
## git stash drop stash@{2}

### Для того, щоб застосувати зміни з контейнерів та видалити контейнер:
## git stash pop

### Для створення мітки з комітом:
## git tag -a v0.0.1 -m "comment" cbaabca
*v0.0.1 - назва мітки*

*cbaabca - назва гілки*

### Для того, щоб відправити конкретну мітку (v0.0.1) на сервер:
## git push origin v0.0.1

### Для того, щоб відправити всі мітки на сервер:
## git push origin --tags

### Для перегляду мітки та зв'язаних з нею об'єктів:
## git show v0.0.1

### Для видалення мітки:
## git tag -d v0.0.1

### Для перегляду міток:
## git tag

### Для відправлення всіх змін конкретної мітки:
## git push origin :refs/tags/v0.0.1
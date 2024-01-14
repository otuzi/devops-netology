# Домашнее задание к занятию «Системы контроля версий»

------

## Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе


### Создание репозитория и первого коммита

1. Зарегистрируйте аккаунт на [https://github.com/](https://github.com/). Если предпочитаете другое хранилище для репозитория, можно использовать его.
2. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием `devops-netology`.
   Обязательно поставьте галочку `Initialize this repository with a README`. 
   
    <img width="976" alt="Screenshot 2024-01-13 at 20 55 02" src="https://github.com/otuzi/devops-netology/assets/61628386/e6875588-d632-4f86-bc16-192d8205f093">

    
3. Создайте [авторизационный токен](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) для клонирования репозитория.
   <img width="1150" alt="Screenshot 2024-01-13 at 21 01 45" src="https://github.com/otuzi/devops-netology/assets/61628386/ee35bd50-5b80-4e1b-99da-555083413972">

5. Склонируйте репозиторий, используя протокол HTTPS (`git clone ...`).
 
    <img width="1160" alt="Screenshot 2024-01-13 at 21 04 13" src="https://github.com/otuzi/devops-netology/assets/61628386/fce715a4-94c3-4921-80e3-f44e6e6dfa5f">

6. Перейдите в каталог с клоном репозитория (`cd devops-netology`).
   <img width="645" alt="Screenshot 2024-01-13 at 21 08 38" src="https://github.com/otuzi/devops-netology/assets/61628386/35f9660c-9228-4026-935e-3893d5eb35a4">

8. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (`git config --global user.name` и `git config --global user.email johndoe@example.com`).
   <img width="626" alt="Screenshot 2024-01-14 at 20 10 46" src="https://github.com/otuzi/devops-netology/assets/61628386/752b68fa-2d49-42d1-9ccc-8235efa38bda">

10. Выполните команду `git status` и запомните результат.
    <img width="673" alt="Screenshot 2024-01-14 at 20 19 00" src="https://github.com/otuzi/devops-netology/assets/61628386/0f7069e8-1190-420a-a3e1-c4ddeb3675d3">

12. Отредактируйте файл `README.md` любым удобным способом, тем самым переведя файл в состояние `Modified`.
14. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага.
    <img width="623" alt="Screenshot 2024-01-14 at 20 20 28" src="https://github.com/otuzi/devops-netology/assets/61628386/5c9cb413-6c15-461c-8265-38cad0a826a7">

16. Теперь посмотрите изменения в файле `README.md`, выполнив команды `git diff` и `git diff --staged`.
    <img width="1187" alt="Screenshot 2024-01-14 at 20 23 04" src="https://github.com/otuzi/devops-netology/assets/61628386/c7fa06e3-4fae-45b1-afd4-df9f660ce166">

18. Переведите файл в состояние `staged` (или, как говорят, просто добавьте файл в коммит) командой `git add README.md`.
    <img width="712" alt="Screenshot 2024-01-14 at 20 26 22" src="https://github.com/otuzi/devops-netology/assets/61628386/30bd51b0-30bf-4963-b579-59d0e7c2d6fa">

20. И ещё раз выполните команды `git diff` и `git diff --staged`. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.
22. Теперь можно сделать коммит `git commit -m 'First commit'`.
    <img width="737" alt="Screenshot 2024-01-14 at 20 27 12" src="https://github.com/otuzi/devops-netology/assets/61628386/c0bc2d30-61fc-44ce-b360-30b180ca7209">

24. И ещё раз посмотреть выводы команд `git status`, `git diff` и `git diff --staged`.
    <img width="500" alt="Screenshot 2024-01-14 at 20 28 14" src="https://github.com/otuzi/devops-netology/assets/61628386/df3d8b21-61f7-4380-8693-a1d276c9520a">


### Создание файлов `.gitignore` и второго коммита

1. Создайте файл `.gitignore` (обратите внимание на точку в начале файла), проверьте его статус сразу после создания. 
1. Добавьте файл `.gitignore` в следующий коммит (`git add...`).
1. На одном из следующих блоков вы будете изучать `Terraform`, давайте сразу создадим соотвествующий каталог `terraform` и внутри этого каталога — файл `.gitignore` по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.  
1. В файле `README.md` опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному `.gitignore`.
1. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть `Added gitignore`.

### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы `will_be_deleted.txt` (с текстом `will_be_deleted`) и `will_be_moved.txt` (с текстом `will_be_moved`) и закоммите их с комментарием `Prepare to delete and move`.
1. В случае необходимости обратитесь к [официальной документации](https://git-scm.com/book/ru/v2/Основы-Git-Запись-изменений-в-репозиторий) — здесь подробно описано, как выполнить следующие шаги. 
1. Удалите файл `will_be_deleted.txt` с диска и из репозитория. 
1. Переименуйте (переместите) файл `will_be_moved.txt` на диске и в репозитории, чтобы он стал называться `has_been_moved.txt`.
1. Закоммитьте результат работы с комментарием `Moved and deleted`.

### Проверка изменения

1. В результате предыдущих шагов в репозитории должно быть как минимум пять коммитов (если вы сделали ещё промежуточные — нет проблем):
    * `Initial Commit` — созданный GitHub при инициализации репозитория. 
    * `First commit` — созданный после изменения файла `README.md`.
    * `Added gitignore` — после добавления `.gitignore`.
    * `Prepare to delete and move` — после добавления двух временных файлов.
    * `Moved and deleted` — после удаления и перемещения временных файлов. 
2. Проверьте это, используя комманду `git log`. Подробно о формате вывода этой команды мы поговорим на следующем занятии, но посмотреть, что она отображает, можно уже сейчас.

### Отправка изменений в репозиторий

Выполните команду `git push`, если Git запросит логин и пароль — введите ваши логин и пароль от GitHub. 

В качестве результата отправьте ссылку на репозиторий. 

----

# Домашнее задание к занятию «Системы контроля версий»

------

## Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе


### Создание репозитория и первого коммита

1. Зарегистрируйте аккаунт на [https://github.com/](https://github.com/). Если предпочитаете другое хранилище для репозитория, можно использовать его.
2. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием `devops-netology`.
   Обязательно поставьте галочку `Initialize this repository with a README`. 
   
   <img width="976" alt="Screenshot 2024-01-13 at 20 55 02" src="https://github.com/otuzi/devops-netology/assets/61628386/88731587-d7ea-4b2c-adfb-6f1f17d55e8d">

3. Создайте [авторизационный токен](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token) для клонирования репозитория.
   <img width="1150" alt="Screenshot 2024-01-13 at 21 01 45" src="https://github.com/otuzi/devops-netology/assets/61628386/9fbf3e78-8d02-4c8d-9b0e-a845df904819">

5. Склонируйте репозиторий, используя протокол HTTPS (`git clone ...`).
 
   <img width="1160" alt="Screenshot 2024-01-13 at 21 04 13" src="https://github.com/otuzi/devops-netology/assets/61628386/47e3ed87-8bbb-4eba-9d90-db5ed0c8aa9a">

6. Перейдите в каталог с клоном репозитория (`cd devops-netology`).
   <img width="645" alt="Screenshot 2024-01-13 at 21 08 38" src="https://github.com/otuzi/devops-netology/assets/61628386/f5e72d52-8472-46ac-a6aa-e37449d173bc">

8. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (`git config --global user.name` и `git config --global user.email johndoe@example.com`).
   <img width="626" alt="Screenshot 2024-01-14 at 20 10 46" src="https://github.com/otuzi/devops-netology/assets/61628386/16cf70e0-d165-424e-a495-8dfb40f05bd5">

10. Выполните команду `git status` и запомните результат.
    <img width="673" alt="Screenshot 2024-01-14 at 20 19 00" src="https://github.com/otuzi/devops-netology/assets/61628386/0f7069e8-1190-420a-a3e1-c4ddeb3675d3">

12. Отредактируйте файл `README.md` любым удобным способом, тем самым переведя файл в состояние `Modified`.
14. Ещё раз выполните `git status` и продолжайте проверять вывод этой команды после каждого следующего шага.
    <img width="623" alt="Screenshot 2024-01-14 at 20 20 28" src="https://github.com/otuzi/devops-netology/assets/61628386/2ed14b9f-f3ef-4a02-b01f-320860c90541">

16. Теперь посмотрите изменения в файле `README.md`, выполнив команды `git diff` и `git diff --staged`.
    <img width="1187" alt="Screenshot 2024-01-14 at 20 23 04" src="https://github.com/otuzi/devops-netology/assets/61628386/20231455-c221-41a2-9863-8e2937d59f86">


18. Переведите файл в состояние `staged` (или, как говорят, просто добавьте файл в коммит) командой `git add README.md`.
    <img width="712" alt="Screenshot 2024-01-14 at 20 26 22" src="https://github.com/otuzi/devops-netology/assets/61628386/bcd5e328-17af-478b-826a-5af3e186633a">

20. И ещё раз выполните команды `git diff` и `git diff --staged`. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.
22. Теперь можно сделать коммит `git commit -m 'First commit'`.
    <img width="737" alt="Screenshot 2024-01-14 at 20 27 12" src="https://github.com/otuzi/devops-netology/assets/61628386/e18ad3a8-bbb5-45a2-870c-886093b23d3f">


24. И ещё раз посмотреть выводы команд `git status`, `git diff` и `git diff --staged`.
    <img width="500" alt="Screenshot 2024-01-14 at 20 28 14" src="https://github.com/otuzi/devops-netology/assets/61628386/50b7942f-d6b7-4d3a-a110-73518e716950">



### Создание файлов `.gitignore` и второго коммита

1. Создайте файл `.gitignore` (обратите внимание на точку в начале файла), проверьте его статус сразу после создания.
   <img width="699" alt="Screenshot 2024-01-14 at 21 15 58" src="https://github.com/otuzi/devops-netology/assets/61628386/a39bc20c-af37-474c-a57b-b9969a9e5529">

2. Добавьте файл `.gitignore` в следующий коммит (`git add...`).
   <img width="714" alt="Screenshot 2024-01-14 at 21 16 31" src="https://github.com/otuzi/devops-netology/assets/61628386/168e2fb9-e6db-4fa6-8f03-b35b6df43038">

3. На одном из следующих блоков вы будете изучать `Terraform`, давайте сразу создадим соотвествующий каталог `terraform` и внутри этого каталога — файл `.gitignore` по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.  
4. В файле `README.md` опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному `.gitignore`.
   
   <img width="736" alt="Screenshot 2024-01-14 at 21 18 32" src="https://github.com/otuzi/devops-netology/assets/61628386/f568ad36-3045-498d-899f-c3d0581ddf23">

   Не будут добавлены в репозиторий файлы которые находятся внутри папки .terraform:
   **/.terraform/*, а также:
   *.tfstate
   *.tfstate.*, а также файлы логов:
   crash.log
   crash.*.log

6. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть `Added gitignore`.
 <img width="633" alt="Screenshot 2024-01-14 at 21 21 40" src="https://github.com/otuzi/devops-netology/assets/61628386/4a3208a4-06ec-4add-ba0a-cb3f9dce7b62">


### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы `will_be_deleted.txt` (с текстом `will_be_deleted`) и `will_be_moved.txt` (с текстом `will_be_moved`) и закоммите их с комментарием `Prepare to delete and move`.
   <img width="666" alt="Screenshot 2024-01-14 at 21 31 16" src="https://github.com/otuzi/devops-netology/assets/61628386/1c1ab2a8-e72d-4de4-9310-53ee8b829be1">

2. В случае необходимости обратитесь к [официальной документации](https://git-scm.com/book/ru/v2/Основы-Git-Запись-изменений-в-репозиторий) — здесь подробно описано, как выполнить следующие шаги. 
3. Удалите файл `will_be_deleted.txt` с диска и из репозитория.
 <img width="1156" alt="Screenshot 2024-01-14 at 21 33 38" src="https://github.com/otuzi/devops-netology/assets/61628386/31d7ca6d-99f0-4297-afcd-c7e2af9be4c9">

4. Переименуйте (переместите) файл `will_be_moved.txt` на диске и в репозитории, чтобы он стал называться `has_been_moved.txt`.
5. Закоммитьте результат работы с комментарием `Moved and deleted`.
<img width="669" alt="Screenshot 2024-01-14 at 21 35 37" src="https://github.com/otuzi/devops-netology/assets/61628386/641ab734-3295-4e06-8feb-44b03031a7e9">

<img width="1121" alt="Screenshot 2024-01-14 at 21 35 53" src="https://github.com/otuzi/devops-netology/assets/61628386/af61db04-cd4a-4cf3-aa0c-b4315115f205">


----

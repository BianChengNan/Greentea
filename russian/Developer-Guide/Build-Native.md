### Краткое руководство по сборке системы

#### Скачивание репозитория с исходным кодом

* Код репозитория займёт **до** 500 (пятисот) мегабайт на диске
* Убедитесь, что скачиваете код в папку **не содержащую пробелов** в пути!
* Перейдите [на страницу репозитория](https://github.com/GreenteaOS/Kernel)
* Если Вы *не* пользуетесь Git то скачайте архив с кодом: <br/> ![image](https://cloud.githubusercontent.com/assets/3642643/19634448/d98f79fa-99c3-11e6-9d3e-009db22395e1.png)
* Для пользователей Git: `git clone --recursive https://github.com/GreenteaOS/Kernel.git`
* Для пользователей [Github for Desktop](https://desktop.github.com): <br/> ![image](https://cloud.githubusercontent.com/assets/3642643/19634404/61125858-99c3-11e6-9c36-60f5a814fcc1.png)
* В этой же папке будут сгенерированы временные файлы в процессе сборки и образы дисков

#### Установка среды сборки

* Скачайте :fire: Flame :fire: [по прямой ссылке](https://github.com/GreenteaOS/Flame/archive/master.zip) или [на странице репозитория](https://github.com/GreenteaOS/Flame) 
* Распакуйте в рекомендуемый путь `C:\Flame` или отредактируйте в `environment.cmd` параметр `TOOLS` при распаковке по нестандартному пути
* Должна получиться папка `C:\Flame` с файлами `version.txt` (версия архива) и остальными (но не вложенная `C:\Flame\Flame`!)

#### Сборка, тестирование и пересборка

* Перед началом сборки убедитесь, что в наличии **не менее гигабайта** свободного места на диске!
* Начальная сборка занимает примерно 40 (сорок) минут, в зависимости от конфигурации ПК
* Запустите из корня репозитория Kernel скрипт `build-bootcd.cmd` (двойным кликом по файлу) или `build-livecd.cmd` для построения установочного или живого диска соответственно
* Для пересборки достаточно снова повторить аналогичную процедуру, это может занимать от пяти секунд до нескольких минут,
от числа затронутых зависимостей и конфигурации ПК
* В папке `output-MinGW-i386` в случае успешной сборки появится `livecd.iso` или `bootcd.iso`

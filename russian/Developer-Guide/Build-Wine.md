### Краткое руководство по сборке системы

Сборка из под иных, чем Windows NT, операционных систем, производится с помощью проекта [Wine](https://www.winehq.org).
Предполагается, что читатель знаком с утилитами **wine** и **winetricks**, настроил их и они готовы к работе.

Процесс радикально ничем не отличается от 
[такого в Windows](https://github.com/GreenteaOS/Greentea/blob/master/russian/Developer-Guide/Build-Native.md), 
за исключением нескольких нюансов.

#### Скачивание репозитория с исходным кодом

Выполните процедуру идентично [оригинальной](https://github.com/GreenteaOS/Greentea/blob/master/russian/Developer-Guide/Build-Native.md).
Репозиторий можно поместить в домашнюю папку (в wine это путь `Z:\home\username\`).

#### Установка среды сборки

Установите среду как в [исходной статье](https://github.com/GreenteaOS/Greentea/blob/master/russian/Developer-Guide/Build-Native.md).

#### Сборка, тестирование и пересборка

Перед выполнением данной процедуры необходимо найти файл `configure.cmd` в папке с кодом, и отредактировать его через gedit:

* Закомментируйте строку, следующую за `REM Detect presence of cmake`, добавлением слова `REM` в начале строки:
<br/>`REM cmd /c cmake --version 2> .....продолжение строки`
* Найдите строку, следующую за `if "%BUILD_ENVIRONMENT%" == "MinGW"`
* В конце строки параметр `"%REACTOS_SOURCE_DIR%"` необходимо заменить на путь к репозиторию (в формате wine), например:
<br/>`"Z:/home/username/Greentea/Kernel"`

Теперь можно открыть через wine ярлык на рабочем столе и выполнить configure, и далее, полностью аналогично исходной статье.

![Travis-Build](https://travis-ci.org/BasePractice/2015.2.svg?branch=master)
Обновление репозитория
======================
Команда выполняется один раз

```
git remote add upstream https://github.com/BasePractice/2015.2.git
```

Команды выполняются каждый раз при обновлении
```
git fetch upstream
git checkout master
git merge upstream/master
```

Удаление  файлов из commit
==============
```
git filter-branch --force --index-filter 'git rm --cached --ignore-unmatch $FILENAME' --prune-empty --tag-name-filter cat -- --all
```

Кусовая работа
==============

Студентам будет предложено два типа курсовых работ:

1.  Программное обеспечение для (пересылки клиентских сообщений) на базе открытого интерфейса социальной сети.
    В квадратных скобках указан функционал данного программного обеспечения. Студенты сами придумывают логику работы. (социальная сеть Вконтакте либо Telegram)
2.  Программное обеспечение для создания и поиска путей в лабиринте. (Генерирование лабиринта с заданными параметрами, создание изображения созданного лабиринта.
    Нахождение путей в гарантированном лабиринте.) [Алгоритмы][http://www.jamisbuck.org/mazes/]

Задания будут раздаваться ```30.10.2015``` года.


Распределение заданий по группам
=================================
[Список](.cources.csv)

Как создать проект вашей курсовой
=================================
[Создание](https://yadi.sk/d/d33U0tWujpScJ)

[Запуск](https://yadi.sk/i/BNaBm1CAjpSeW)


Правила игры
=================================

1.  Необходимые, но не достаточные условия приемки исходного кода курсовой
    -  Не использовать стандартные потоки ввода/вывода `System.out, System.err, System.in`
    -  Использовать `Logger` для вывода ошибок, информации, отладочной информации. Также следует использовать шаблоны вывода `{}`, а не 
       конкатенацию строк `+`
    -  Обязательно обрабатывать ошибки, не проглатывать их
    -  Обрабатывать ошибки надо раздельно, записывая в лог с адекватным описанием
    -  Код должен соответствовать `Java Code Conventions` [JCC](http://www.oracle.com/technetwork/java/codeconventions-150003.pdf)
    -  Не вносить изменения в основной модуль и модули других студентов. Исключительно следует вносить изменения в свой модуль
    -  В случае, если вам требуется внести изменения в не свой модуль, следует оформить изменения отдельным `commit` и в описании написать
       для чего вы это делаете и зачем
    -  Применять только уже используемые библиотеки. При внесении новой библиотеки следует в комментарии написать для чего она вам нужена и 
       почему функционал ранее используемых библиотек вас не устраивает
    -  Настройки, дополнительные файлы, словари следует сохранять в ресурсах
    -  По возможности использовать `try-with-resources` везде где можно
    -  Освобождать ранее выделенные ресурсы

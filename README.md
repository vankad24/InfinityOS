# Операционная система Infinity
## Требования
- Возможность запускать linux программы, android приложения и, как минимум, частичную поддержку windows программ. Возможно, посредством симуляции файловой системы этих ОС.
- Возможность легко собирать свой образ, чтобы потом не устанавливать все эти программы.
- Возможность экспортировать все настройки, чтобы потом не делать это снова после переустановки. Доступен экспорт в виде файла или строки в base64
- Возможность добавлять свои сочетания клавиш.
- Live версия, чтобы больше пользователей могли попробовать.
- Когда файл открыт в другой программе, чтобы сразу писало в какой и id процесса
- Возможность настройки контекстного меню
- Возможность создать файл с помощью сочетаний клавиш в проводнике
- Возможность проверить операционную систему на целостность, как это умеют делать некоторые игры. При необходимости, скачает файлы с сервера.
- В настройках устройства можно зайти в раздел "драйвера", где будут показаны доступные версии и ссылки на источники (например, оф сайты производителей).
- Обучение с подсказками при первом запуске.

## Файловая система
- `/` в путях файлов
- Некоторые системные приложения, такие как проводник, имеют разрешение на доступ к файловой системе, поэтому через него можно свободно смотреть файлы и перемещаться, в том числе в личные папки программ.
- Для запуска файлов используются расширения, как в windows. Запускаемые файлы будут помечаться как .run (аналог .exe в windows).
Реестр?

## Внешний вид
- Все приложения для отображения интерфейсов, кнопок и рисования используют API операционной системы и могут использовать уже готовые кнопки, тестовые поля и так далее, но могут и создать свои, наследуясь и переопределяя view (как в android).
- За интерфейс, рабочий стол, пуск, бар, уведомления и другие кнопочки отвечает лаунчер, как в android. Но в отличии от него, лаунчер также отвечает за отображение всех других приложений. Помимо стиля, цветов и краёв окон, лаунчер переопределяет стандартные view. То есть, установив новый лаунчер, все приложения, которые используют внутри себя стандартные view, такие как кнопки, текстовые поля, выбор даты, выбор цвета, ползунок громкости, анимации нажатия и т.д. будут выглядеть по-другому. Если лаунчер не переопределил какой-то view, будет использован view из стандартного лаунчера операционной системы.
- В настройках можно поменять тип меню и нижней панели бара (справа, слева, внизу, по центру).


## Установка программ
- Установка программ осуществляется специальным установщиком пакетов, которые имеют расширение `.app` (альтернатива `.apk` в android). Пользователь может выбрать диск, на который установить эту программу, но не папку. Папку (например, `c://programs`) выбирает операционная система. Разработчик программы тоже не может выбрать место установки его программы (чтобы не устанавливать куда попало).
- После установки для каждой программы создаётся своя папка. Она является корневой при запуске программы. В ней программист может делать что хочет: создавать файлы, папки и удалять их. Чтобы получить доступ вне, приложению нужно получить высокое разрешение от пользователя (как в android). При удалении программы удаляется вся эта папка. Есть общие папки, такие как `Документы` или `Изображения`. Для получения к ним доступа, нужно тоже разрешение от пользователя, но не такое высокое.
- После установки программа не создаёт ярлыки для запуска. Она помещается в список установленных программ. Этот список потом использует лаунчер и уже он отображает иконки. Из этого же списка можно добавить программы в список программ автозапуска.
- Возможность запускать программы как исполняемые файлы, всё ещё остаётся, но с некоторыми ограничениями. Такой тип программ используется только программистами при разработке, пиратами и вирусами. Поэтому, такие программы по умолчанию могут запускаться только в `c://dev` и не имеют доступа к другим папкам системы, эти права нужно предоставлять. Но, в основном, даже для пиратских программ, используются установочные пакеты и в запускаемых программах нет особой необходимости. 
- Infinity OS имеет свой магазин приложений, как microsoft store. Есть возможность устанавливать консольные программы через пакетный менеджер (репозиторий), который имеет 3 стадии проверки пакетов (по типу `pacman` в manjaro linux).


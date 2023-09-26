# Операционная система Infinity
## Основные требования
- Обязательный пункт: на разных разрешениях интерфейс должен выглядеть нормально. У linux, например, с этим проблемы.
- Полная поддержка windows программ и, как минимум, частичная поддержка linux программ и android приложений. Возможно, посредством симуляции окружения или файловой системы этих ОС. То есть, например, за windows программы отвечает отдельное приложение "InfiWin", которое в своей директории приложения имеет папки "Users", "Program Files", "AppData", куда оно и устанавливает windows программы, а в саму InfinityOS просто добавляет ярлыки для запуска этих приложений. Такие программы будут запускаться в окне, как и обычные программы, только они будут думать, что они в windows, хотя они просто под руководством "InfiWin".
- Важно сделать поддержку игр для развития популярности ОС.
- Обучение с подсказками при первом запуске.
- Возможность создавать несколько рабочих столов (разные ярлыки и обои)
## Установка
- Возможность легко собирать свой образ без сторонних программ, чтобы потом установить свой свой образ с готовыми программами.
- Live версия, чтобы больше пользователей могли попробовать.
- В настройках есть кнопка "проверка целостности системы", которая проверит все системные файлы и, в случае необходимости, скачает их заново с сервера. Такая функция проверки файлов сделана в некоторых играх. Можно проверять за счёт хэша от файлов.
- Терминал из коробки zsh или fish, а не какой-нибудь bash.
- При установке можно выбрать количество предустановленных приложений: минимальное, стандартное, расширенное. В расширенном будут все эмуляторы: андроид, линукс, винда.
## Настройки
- Возможность экспортировать все настройки, чтобы потом не делать это снова после переустановки. Доступен экспорт в виде файла или строки в base64.
- Возможность добавлять свои сочетания клавиш.
- Есть раздел, в котором расширения сгруппированы по типу файлов. Это просто значения, разделённые пробелом, их можно менять. Пример:
```
Текст: txt text
Документы: doc pdf
Изображения: jpg png bmp
Программы: java py cpp
Бинарные: bin class
Исполняемые: exe run
```
- Возможность настройки контекстного меню. Можно настроить пункты для рабочего стола, проводника и, даже, для конкретного расширения файла или группы расширений (например, изображения). Также, можно настроить сочетание клавиш, для вызова этого пункта. Подсказка о сочетании клавиш пишется, когда вызываешь контекстное меню.
- В настройках устройства можно зайти в раздел "драйвера", где будут показаны доступные версии и ссылки на источники (например, оф сайты производителей).
- В настройках можно запустить тест для проверки дисплея (включать разные цвета и яркость)
- Чтобы в ОС сохранялись настройки монитора и после его переподключения не сбрасывалась частота кадров, разрешение, размер интерфейса и другие настройки.
- Возможность сделать сетевую папку так же просто, как включить блютуз
- Ползунок с выбором размера интерфейса в процентах.
- Возле большинства пунктов в настройках есть значок "?", при наведении на который всплывает пояснение, за что отвечает эта настройка.
## Диспетчер задач
- Вкладка, где можно посмотреть, какая программа открыла какой файл.
- Автозапуск. Как на андроид, там отображается список приложений, где можно нажать на переключатель, чтобы выключить/включить автозапуск. Можно добавить стороннее приложение (для исполняемых файлов) или команду.
- Системно важные процессы специально помечены, чтобы их случайно не завершить.
- Вкладка, где можно посмотреть, какие программы не дают компьютеру уснуть.

## Внешние устройства
- Гибкая работа с несколькими экранами. Например, поддержка двух мышек для управления разными приложениями на разных мониторах.
- Возможность управлять компьютером только геймпадом. То есть возможность перемещаться по интерфейсу, закрывать, сворачивать программы, открывать меню пуск. Самый простой способ - управлять мышью с помощью джойстиков (левый двигает мышку, правый прокручивает страницу).
- Управление мышью компьютера с помощью клавиатуры. Например, win + стрелочки.
- Возможность использовать беспроводное устройство как дополнительный экран. Причем, если, например, телевизор не поддерживает chromecast, то на него можно установить специальное приложение.
- Два компьютера с ОС infinity можно использовать совместно и управлять одной мышью (передвигать мышь с одного устройства на другое и перетаскивать файлы)  
 - Если подключено несколько мониторов, на каждом из них можно запустить своего пользователя. Если запустить одного и того же пользователя, оно будет работать так же, как и на винде. Если разных, то приложения будут работать как на разных компьютерах. То есть имея две монитора, мышки и клавиатуры можно пользоваться одним компьютером, как двумя
 - Возможность беспроводной трансляции картинки на другой монитор через miracast, chromecast и свою собственную реализацию трансляции.
## Файлы и проводник
- `/` в путях файлов
- Некоторые системные приложения, такие как проводник, имеют разрешение на доступ к файловой системе, поэтому через него можно свободно смотреть файлы и перемещаться, в том числе в личные папки программ.
- Для запуска файлов используются расширения, как в windows. Запускаемые файлы будут помечаться как .run (аналог .exe в windows).
- Можно указать, какая папка будет открываться при открытии проводника.
- Файл или ярлык в проводнике можно открыть с помощью Shift+Enter или вызвать из контекстного меню "открыть с помощью". Откроется всплывающее окно, в котором можно выбрать одно из недавно использованных приложений, найти приложение через поиск, указать галочку "Использовать всегда при открытии таких файлов" или нажать кнопку, чтобы перейти в настройки в раздел "Приложения по умолчанию".
- Возможность создать файл с помощью сочетаний клавиш в проводнике
- При удалении файла, если этот файл открыт в другой программе, откроется окно, в котором будет написано название этой программы и id процесса синим цветом. При нажатии на этот id процесса откроется диспетчер задач, где будет выделен это процесс.
- По умолчанию расширения файлов не пишутся, но если нажать "переименовать файл", расширение отобразится. В настройках можно включить, чтобы расширения отображались всегда.
Реестр?

## Внешний вид
- Все приложения для отображения интерфейсов, кнопок и рисования используют API операционной системы и могут использовать уже готовые кнопки, тестовые поля и так далее, но могут и создать свои, наследуясь и переопределяя view (как в android).
- За интерфейс, рабочий стол, пуск, бар, уведомления и другие кнопочки отвечает лаунчер, как в android. Но в отличии от него, лаунчер также отвечает за отображение всех других приложений. Помимо стиля, цветов и краёв окон, лаунчер переопределяет стандартные view. То есть, установив новый лаунчер, все приложения, которые используют внутри себя стандартные view, такие как кнопки, текстовые поля, выбор даты, выбор цвета, ползунок громкости, анимации нажатия и т.д. будут выглядеть по-другому. Если лаунчер не переопределил какой-то view, будет использован view из стандартного лаунчера операционной системы.
- В настройках можно поменять тип меню и нижней панели бара (справа, слева, внизу, по центру).
- Возможность менять курсор, иконки и звуки. Причём сразу из коробки есть небольшой выбор. Если хочется что-то другое, то прямо там же в настройках можно нажать кнопку, которая переведёт в магазин приложений, где можно установить пользовательский курсор, иконки или звуки.
- По умолчанию при нажатии кнопки win открывается меню, как на windows10, но при двойном нажатии win открывается меню всех приложений, как на ubuntu. Приложение из этого меню можно перетащить и поместить на рабочий стол, как на android. Приложения можно перетаскивать на друг друга и создавать папки. Внешний вид, тип меню, сочетания клавиш для открытия, иконки, картинку на кнопке меню и другое можно изменить в настройках.
- Кнопки свернуть, развернуть, закрыть выглядят как тонкие прямоугольники синего, фиолетового и красного цвета соответственно. При наведении на кнопки, они разворачиваются в прямоугольники с иконками, как на windows.
- Скруглённые края, тени и анимации для эстетического наслаждения и привлечения внимания.
- Открытая вкладка приложения (внизу в баре) принимает тот же цвет, что и открытое приложение и выглядит так, будто они соединяются. Как вкладки в яндекс браузере
- Кнопка обычного выключения компьютера и кнопка быстрого выключения (гибернация).
- При печати текста появляются подсказки. На android подсказки есть, что очень удобно. Поэтому, почему бы их не сделать на компьютере? Причём с настройками словаря и авто дополнения.
- На F12 можно посмотреть разметку интерфейса приложения, как в браузере. Также можно посмотреть скрипты, которые обрабатывают нажатия на кнопки и подобное.

## Программы
- Установка программ осуществляется специальным установщиком пакетов, которые имеют расширение `.app` (альтернатива `.apk` в android). Пользователь может выбрать диск, на который установить эту программу, но не папку. Папку (например, `c://programs`) выбирает операционная система. Разработчик программы тоже не может выбрать место установки его программы (чтобы не устанавливать куда попало).
- После установки для каждой программы создаётся своя папка. Она является корневой при запуске программы. В ней программист может делать что хочет: создавать файлы, папки и удалять их. Чтобы получить доступ вне, приложению нужно получить высокое разрешение от пользователя (как в android). При удалении программы удаляется вся эта папка. Есть общие папки, такие как `Документы` или `Изображения`. Для получения к ним доступа, нужно тоже разрешение от пользователя, но не такое высокое.
- После установки программа не создаёт ярлыки для запуска. Она помещается в список установленных программ. Этот список потом использует лаунчер и уже он отображает иконки. Из этого же списка можно добавить программы в список программ автозапуска.
- Возможность запускать программы как исполняемые файлы, всё ещё остаётся, но с некоторыми ограничениями. Такой тип программ используется только программистами при разработке, пиратами и вирусами. Поэтому, такие программы по умолчанию могут запускаться только в `c://dev` и не имеют доступа к другим папкам системы, эти права нужно предоставлять. Но, в основном, даже для пиратских программ, используются установочные пакеты и в запускаемых программах нет особой необходимости. 
- Infinity OS имеет свой магазин приложений, как microsoft store. Есть возможность устанавливать консольные программы через пакетный менеджер (репозиторий), который имеет 3 стадии проверки пакетов (по типу `pacman` в manjaro linux).
- Для разработчиков приложений предоставляется специальное API для взаимодействия с ОС. Поддерживается написание приложений на популярных языках программирования и на Aqua lang.
- Графическая часть приложений в ОС работает на подобии браузерного движка. Интерфейсы в приложениях создаются не с помощью xml, как это делают в android, а с помощью своего HTML и своего языка стилей CSL (Cascade Style Language), который похож на CSS, но имеет гораздо меньше бесполезных свойств и свойства сгруппированы по классам. Например, `grid.columns: 5;`. Эти стили можно менять на свои.
- Если нет приложения для открытия данного расширения, то вылезет всплывающее меню, где будет показан топ приложений для открытия этого файла.  
- Возможность перенести приложение на другое устройство со всеми сохранениями. Например, в настройках приложения сделать кнопку "Импортировать с сохранениями", которая создаст модифицированный `.app` файл.
- Возможность собирать запускаемые архивы (по типу jar), которые умеет запускать ОС. Это обычны архив, просто ОС умеет считывать оттуда конфиг, а после этого запускать main, который тоже находится внутри архива. Именно так могут быть устроены пакеты установочных программ. В android apk файлы - тоже архивы.


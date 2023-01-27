## Part 1. Установка ОС

- ``Смотрим версию Ubuntu после установки ``<br>
![Alt text](../misc/images/1.png "Optional Title")<br>


---

## Part 2. Создание пользователя
- ``Создаём пользователя и назначаем ему группу adm``<br>
![Alt text](../misc/images/2.png "Optional Title")<br>


- ``Вывод списка пользователей (новый юзер в конце списка)``<br>
![Alt text](../misc/images/22.png "Optional Title")<br>


---

## Part 3. Настройка сети ОС

- ``Установили новое имя машины и вывели его в терминал``<br>
![Alt text](../misc/images/31.png "Optional Title")<br>

- ``Установили новую временную зону и вывели информацию в терминал``<br>
![Alt text](../misc/images/32.png "Optional Title")<br>

- ``Установили набор сетевых инструментов``<br>
![Alt text](../misc/images/33.png "Optional Title")<br>
``Вывели информацию о сетевых интерфейсах``<br>
![Alt text](../misc/images/34.png "Optional Title")<br>
**lo (loopback device)** – виртуальный интерфейс, присутствующий по умолчанию в любом Linux. Он используется для отладки сетевых программ и запуска серверных приложений на локальной машине. С этим интерфейсом всегда связан адрес 127.0.0.1. У него есть dns-имя – localhost.

- ``Удалили старый и получили новый ip от dhcp сервера``<br>
![Alt text](../misc/images/36.png "Optional Title")<br>
**DHCP - Dynamic Host Configuration Protocol**

- ``Узнали внешний IP-адрес``<br>
![Alt text](../misc/images/38.png "Optional Title")<br>

- ``Узнали внутренний IP-адрес шлюза, он же ip-адрес по умолчанию``<br>
![Alt text](../misc/images/37.png "Optional Title")<br>

- ``Изменили файл /etc/netplan/*.yaml, применили изменения в netplan, перезагрузились``<br>
![Alt text](../misc/images/311.png "Optional Title")<br>
![Alt text](../misc/images/39.png "Optional Title")<br>
- ``Проверяем, что адреса соотсветствуют заданным в предыдущем пункте``<br>
![Alt text](../misc/images/310.png "Optional Title")<br>
- ``Успешно пропинговали удаленные хосты 1.1.1.1 и ya.ru``<br>
![Alt text](../misc/images/312.png "Optional Title")<br>

---

## Part 4. Обновление ОС
- ``Успешно обновили системыне пакеты``<br>
![Alt text](../misc/images/4.png "Optional Title")<br>

---

## Part 5. Использование команды sudo
- **sudo** - позволяет временно поднимать привилегии и выполнять задачи администрирования системы с максимальными правами<br>
``Добавили пользователя в группу с привилегиями sudo, переключились на этого пользователя и поменяли hostname``<br>
![Alt text](../misc/images/5.png "Optional Title")<br>

---

## Part 6. Установка и настройка службы времени
- ``Вывод команды с корректным временем``<br>
![Alt text](../misc/images/6.png "Optional Title")<br>

---

## Part 7. Установка и использование текстовых редакторов
- ``**VIM** Для сохранения и выхода нажал ESC и прописал :wq и имя документа``<br>
![Alt text](../misc/images/71.png "Optional Title")<br>
- ``**NANO** Для сохранения нажал ^O, ввёл имя файла и подтвердил. Вышел через ^X``<br>
![Alt text](../misc/images/72.png "Optional Title")<br>
- ``**JOE** Для сохранения и выхода нажал ^KX, ввёл имя файла и подтвердил.``<br>
![Alt text](../misc/images/73.png "Optional Title")<br>

- ``**VIM** Для выхода без сохранения ESC -> :q! -> ENTER``<br>
![Alt text](../misc/images/74.png "Optional Title")<br>
- ``**NANO** Для выхода без сохранения ^X -> N``<br>
![Alt text](../misc/images/75.png "Optional Title")<br>
- ``**JOE** Для выхода без сохранения ^C -> y``<br>
![Alt text](../misc/images/76.png "Optional Title")<br>
- ``**VIM** Для поиска: /что_ищем``<br>
![Alt text](../misc/images/77.png "Optional Title")<br>
- ``**VIM** Для замены: :s/что_заменить/чем``<br>
![Alt text](../misc/images/78.png "Optional Title")<br>
- ``**NANO** Для поиска: ^W -> что ищем``<br>
![Alt text](../misc/images/79.png "Optional Title")<br>
- ``**NANO** Для замены: ^\ -> что заменить -> чем -> Y``<br>
![Alt text](../misc/images/710.png "Optional Title")<br>
- ``**JOE** Для поиска: ^K F -> что ищем -> I``<br>
![Alt text](../misc/images/711.png "Optional Title")<br>
- ``**JOE** Для замены: ^K F -> что заменить -> R -> чем -> Y``<br>
![Alt text](../misc/images/712.png "Optional Title")<br>

---

## Part 8. Установка и базовая настройка сервиса SSHD
- ``Установил openssh-server и настроил конфиг``<br>
- ``Выполнил sudo systemctl start sshd``<br>
- ``Выполнил sudo systemctl enable sshd``<br>
- ``Отобразил наличие процесса``<br>
**ps** - выводит сведения о процессах в статическом виде<br>
**-e** - позволяет выбрать все процессы<br>
**| grep sshd** - поиск по выводу через пайп<br>
![Alt text](../misc/images/81.png "Optional Title")<br>
- ``reboot``<br>
- ``netstat -tan``<br>
![Alt text](../misc/images/82.png "Optional Title")<br>
**-tan**: <br>
-a -	Показывать состояние всех сокетов; обычно сокеты, используемые серверными процессами, не показываются.<br>
-n - Показывать сетевые адреса как числа. netstat обычно показывает адреса как символы.<br>
-t - Отображать TCP подключения<br>
**Proto** - Содержит тип протокола<br>
**Recv-Q** - Счётчик байтов не скопированных программой пользователя из этого сокета.<br>
**Send-Q** - Счётчик байтов, не подтверждённых удалённым узлом.<br>
**Local Address** - Адрес и номер порта локального конца сокета.<br>
**Foreign Address** - Адрес и номер порта удалённого конца сокета.<br>
**State** - Состояние сокета.<br> 
LISTEN Сокет ожидает входящих подключений.<br> 
SYN_SENT Сокет, находящийся в режиме активной попытки установки подключения.<br>
0.0.0.0 -  это немаршрутизируемый адрес IPv4, который используется в качестве адреса по умолчанию или адреса-заполнителя.
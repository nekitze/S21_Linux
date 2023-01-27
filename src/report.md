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

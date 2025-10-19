## Часть 1. Инструмент ipcalc

* сетевой адрес 192.167.38.54/13

<figure>
    <img src="./screen/Part_1.png" alt="Part_1" />
    <figcaption ></figcaption>
</figure> 

* Маска 255.255.255.0

	- в префиксной записи /24
	- в двоичной записи 11111111.11111111.11111111.00000000
	
<figure>
    <img src="./screen/Part_1_1.png" alt="Part_1_1" />
    <figcaption ></figcaption>
</figure>   
	
* Маска /15

	- маска 255.254.0.0
	- в двоичной записи 11111111.11111111.00000000.00000000
<figure>
    <img src="./screen/Part_1_2.png" alt="Part_1_2" />
    <figcaption ></figcaption>
</figure>

* Маска 11111111.11111111.11111111.11110000

	По таблице сетевых масок вычислил маску сети и префикс,
	так как ipcalc не поддерживает двоичную форму записи
	- маска 255.255.255.240
	- в префиксной записи /28

<figure>
    <img src="./screen/Part_1_3.png" alt="Part_1_3" />
    <figcaption ></figcaption>
</figure>

Проверяем, берем любой ip

<figure>
    <img src="./screen/Part_1_4.png" alt="Part_1_4" />
    <figcaption ></figcaption> 
</figure>


* ipcalc 12.167.38.4/8

	- минимальный хост 12.0.0.1
	- максимальный хост 12.255.255.254

<figure>
    <img src="./screen/Part_1_5.png" alt="Part_1_5" />
    <figcaption ></figcaption> 
</figure>

* 11111111.11111111.00000000.00000000 -> ipcalc 12.167.38.4/16

	- минимальный хост 12.167.0.1
	- максимальный хост 12.167.255.254

<figure>
    <img src="./screen/Part_1_6.png" alt="Part_1_6" />
    <figcaption ></figcaption> 
</figure>


* ipcalc 12.167.38.4/255.255.254.0

	- минимальный хост 12.167.38.1
	- максимальный хост 12.167.39.254 

<figure>
    <img src="./screen/Part_1_7.png" alt="Part_1_7" />
    <figcaption ></figcaption> 
</figure>

* ipcalc 12.167.38.4/4

	- минимальный хост 0.0.0.1
	- максимальный хост 12.255.255.254 

<figure>
    <img src="./screen/Part_1_7_1.png" alt="Part_1_7_1" />
    <figcaption ></figcaption> 
</figure>

* В самой последней строчке Hosts/Net пишется либо класс интернета, либо looopback, что значит айпи адрес внутренний
	
127.0.0.0 — 127.255.255.255 (зарезервировано для петлевых интерфейсов (не используется для обмена между узлами сети), т. н. localhost).

- 194.34.23.100 не является адресом локального 
	хоста, не входит в диапазон

<figure>
    <img src="./screen/Part_1_8.png" alt="Part_1_8" />
    <figcaption ></figcaption> 
</figure> 

- 127.0.0.2 является частью диапазона адресов localhost
	
<figure>
    <img src="./screen/Part_1_9.png" alt="Part_1_9" />
    <figcaption ></figcaption> 
</figure> 

- 127.1.0.1 является частью диапазона адресов localhost

<figure>
    <img src="./screen/Part_1_10.png" alt="Part_1_10" />
    <figcaption ></figcaption>  
</figure>

- 128.0.0.1 не является адресом локального хоста, не входит в диапазон

<figure>
    <img src="./screen/Part_1_11.png" alt="Part_1_11" />
    <figcaption ></figcaption> 
</figure> 

Итого к приложению localhost:
    - можно получить доступ по адресам 127.0.0.2, 127.1.0.1
    - нельзя получить доступ по адресам 194.34.23.100, 128.0.0.1 

Так же с помощью команды ipcalc мы можем посмотреть находится ли этот айпи адрес в списке частных или публичных сетей.

- 10.0.0.45 частный

<figure>
    <img src="./screen/Part_1_12.png" alt="Part_1_12" />
    <figcaption ></figcaption> 
</figure> 

- 134.43.0.2 публичный

<figure>
    <img src="./screen/Part_1_13.png" alt="Part_1_13" />
    <figcaption ></figcaption> 
</figure> 

- 192.168.4.2 частный

<figure>
    <img src="./screen/Part_1_14.png" alt="Part_1_14" />
    <figcaption ></figcaption> 
</figure> 

- 172.20.250.4 частный

<figure>
    <img src="./screen/Part_1_15.png" alt="Part_1_15" />
    <figcaption ></figcaption> 
</figure> 

- 172.0.2.1 публичный

<figure>
    <img src="./screen/Part_1_16.png" alt="Part_1_16" />
    <figcaption ></figcaption> 
</figure> 

- 192.172.0.1 публичный

<figure>
    <img src="./screen/Part_1_17.png" alt="Part_1_17" />
    <figcaption ></figcaption> 
</figure> 

- 172.68.0.2 публичный
 
<figure>
    <img src="./screen/Part_1_18.png" alt="Part_1_18" />
    <figcaption ></figcaption> 
</figure> 
  
- 172.16.255.255 частный

<figure>
    <img src="./screen/Part_1_19.png" alt="Part_1_19" />
    <figcaption ></figcaption> 
</figure> 

- 10.10.10.10 частный

<figure>
    <img src="./screen/Part_1_20.png" alt="Part_1_20" />
    <figcaption ></figcaption> 
</figure> 

- 192.169.168.1 публичный

<figure>
    <img src="./screen/Part_1_21.png" alt="Part_1_21" />
    <figcaption ></figcaption> 
</figure> 

* какие из перечисленных IP-адресов шлюза возможны для сети 10.10.0.0/18 : 10.0.0.1 , 10.10.0.2 , 10.10.10.10 , 10.10.100.1 , 10.10.1.255

 
<figure>
    <img src="./screen/Part_1_22.png" alt="Part_1_22" />
    <figcaption ></figcaption> 
</figure> 
	
	Диапазон IP адресов для сети 10.10.0.0/18 
	HostMin: 10.10.0.1
	HostMax: 10.10.63.254
	
	поэтому возможны для сети 10.10.0.0/18: 
	10.10.0.2
	10.10.10.10
	10.10.1.255

    не может имкеть ip:
    10.0.0.1
    10.10.100.1


## Часть 2. Статическая маршрутизация между двумя машинами



**ws1**

<figure>
    <img src="./screen/Part_2_3.png" alt="Part_2_3" />
    <figcaption ></figcaption> 
</figure> 

**ws2**
 
<figure>
    <img src="./screen/Part_2_4.png" alt="Part_2_4" />
    <figcaption ></figcaption> 
</figure> 

* Выполните netplan apply команду для перезапуска сетевой службы.

ws1

<figure>
    <img src="./screen/Part_2_5.png" alt="Part_2_5" />
    <figcaption ></figcaption> 
</figure> 

ws2 

<figure>
    <img src="./screen/Part_2_6.png" alt="Part_2_6" />
    <figcaption ></figcaption> 
</figure> 

1 Добавление статического маршрута вручную

* Добавьте статический маршрут от одной машины к другой. Проверьте соединение между машинами

ws1

<figure>
    <img src="./screen/Part_2_7.png" alt="Part_2_7" />
    <figcaption ></figcaption> 
</figure> 

ws2 

<figure>
    <img src="./screen/Part_2_8.png" alt="Part_2_8" />
    <figcaption ></figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_2_9.png" alt="Part_2_9" />
    <figcaption ></figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_2_10.png" alt="Part_2_10" />
    <figcaption ></figcaption> 
</figure> 


2 Добавление статического маршрута с сохранением

* Добавьте статический маршрут с одной машины на другую с помощью файла /etc/netplan/00-installer-config.yaml

<figure>
    <img src="./screen/Part_2_11.png" alt="Part_2_11" />
    <figcaption ></figcaption> 
</figure> 


* Проверьте соединение между машинами. 

<figure>
    <img src="./screen/Part_2_12.png" alt="Part_2_12" />
    <figcaption ></figcaption> 
</figure> 

## Часть 3. Утилита iperf3

1. Скорость соединения

* Конвертируйте и запишите результаты в отчет: 8 Мбит/с в МБ/с, 100 МБ/с в Кбит/с, 1 Гбит/с в Мбит/с

	- 8 Мбит/с - 1 МБ/c
	- 100 МБ/с - 800 000 Кбит/с
	- 1 Гбит/с - 1000 Мбит/с

2. утилита iperf3

* Измерьте скорость соединения между ws1 и ws2

ws1

<figure>
    <img src="./screen/Part_3_1.png" alt="Part_3_1" />
    <figcaption ></figcaption> 
</figure> 

ws2 

<figure>
    <img src="./screen/Part_3_2.png" alt="Part_3_2" />
    <figcaption ></figcaption> 
</figure> 
 


## Часть 4. Сетевой брандмауэр

<figure>
    <img src="./screen/Part_4_1.png" alt="Part_4_1" />
    <figcaption></figcaption> 
</figure>
   
<figure>
    <img src="./screen/Part_4_2.png" alt="Part_4_2" />
    <figcaption></figcaption> 
</figure>

<figure>
    <img src="./screen/Part_4_3.png" alt="Part_4_3" />
    <figcaption></figcaption> 
</figure>

Флаг -j в команде iptables используется для указания целевого действия, которое должно быть выполнено, если пакет соответствует заданным условиям в правиле. Так как на машине ws1 первым срабатывает правило DROP, то пакет отбрасывается и пинг от ws2 до ws1 не будет работать. Разрешающее правило, которое идет следующим уже не срабатывает. На ws2 первым действием срабатывает ACCEPT, пакет принимается и пинг работает.
	
2. Утилита nmap

* Используйте команду ping , чтобы найти машину, которая не пингуется, затем используйте утилиту nmap, чтобы показать, что хост машины работает

<figure>
    <img src="./screen/Part_4_4.png" alt="Part_4_4" />
    <figcaption></figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_4_5.png" alt="Part_4_5" />
    <figcaption></figcaption> 
</figure> 

* Разница между стратегиями, применёнными в первом и втором файлах (/etc/firewall.sh на ws1 и ws2), заключается в порядке написания правил и их эффекте на работу файрвола.

    Стратегия на ws1 Сначала применяется запрещающее правило для ICMP (пинг). Затем добавляется разрешающее правило, которое перезаписывает предыдущее, чтобы разрешить ICMP.
    В данном случае запрещающее правило становится неэффективным, поскольку разрешающее правило, добавленное после него, перекрывает действие запрета. Итоговое поведение машины: ICMP разрешён (пинг работает).

    Стратегия на ws2 Сначала применяется разрешающее правило для ICMP (пинг). Затем добавляется запрещающее правило, которое перезаписывает предыдущее, чтобы заблокировать ICMP.
    В данном случае разрешающее правило становится неэффективным, поскольку запрещающее правило, добавленное после него, перекрывает действие разрешения. Итоговое поведение машины: ICMP запрещён (пинг не работает).

    Флаг -j (действие): Этот флаг определяет, что делать с пакетом, если он подходит под условия правила. Именно последовательная проверка и раннее применение действия на первом совпадающем правиле определяют итоговое поведение. В правилах iptables важно учитывать порядок, особенно если используются как разрешающие (ACCEPT), так и запрещающие (DROP) действия. Обычно сначала задаются общие правила (например, разрешение базовых соединений), а затем блокируются более специфичные или оставшиеся соединения.

## Часть 5. Статическая сетевая маршрутизация

* Настройка адресов машин
* скрины с содержанием файла etc/netplan/00-installer-config.yaml для каждой машины

<figure>
    <img src="./screen/Part_5_1.png" alt="Part_5_1" />
    <figcaption>ws11</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_2.png" alt="Part_5_2" />
    <figcaption>ws21</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_3.png" alt="Part_5_3" />
    <figcaption>ws22</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_4.png" alt="Part_5_4" />
    <figcaption>r1</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_5.png" alt="Part_5_5" />
    <figcaption>r2</figcaption> 
</figure> 

* вызов команд netplan apply, ip -4 a проверить, что адрес машины задан верно.

<figure>
    <img src="./screen/Part_5_6.png" alt="Part_5_6" />
    <figcaption>ws11</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_7.png" alt="Part_5_7" />
    <figcaption>ws21</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_8.png" alt="Part_5_8" />
    <figcaption>ws22</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_9.png" alt="Part_5_9" />
    <figcaption>r1</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_10.png" alt="Part_5_10" />
    <figcaption>r2</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_11.png" alt="Part_5_11" />
    <figcaption>пинг ws22 с ws21</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_12.png" alt="Part_5_12" />
    <figcaption>пинг r1 с ws11</figcaption> 
</figure> 

* Включение переадресации IP-адресов

<figure>
    <img src="./screen/Part_5_13.png" alt="Part_5_13" />
    <figcaption>r1 вызов команды sysctl -w net.ipv4.ip_forward=1</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_14.png" alt="Part_5_14" />
    <figcaption>r2 вызов команды sysctl -w net.ipv4.ip_forward=1</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_15.png" alt="Part_5_15" />
    <figcaption> r1 добавил строку net.ipv4.ip_forward = 1 </figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_16.png" alt="Part_5_16" />
    <figcaption>r2 добавил строку net.ipv4.ip_forward = 1</figcaption> 
</figure> 

* Установка маршрута по умолчанию

<figure>
    <img src="./screen/Part_5_17.png" alt="Part_5_17" />
    <figcaption>ws11 netplan</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_18.png" alt="Part_5_18" />
    <figcaption>ws21 netplan</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_19.png" alt="Part_5_19" />
    <figcaption>ws22 netplan</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_20.png" alt="Part_5_20" />
    <figcaption>ws11 ip r</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_21.png" alt="Part_5_21" />
    <figcaption>ws21 ip r</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_22.png" alt="Part_5_22" />
    <figcaption>ws22 ip r</figcaption> 
</figure> 

Пропингуй с ws11 роутер r2 и покажи на r2, что пинг доходит. Для этого используй команду: tcpdump -tn -i eth0

<figure>
    <img src="./screen/Part_5_23.png" alt="Part_5_23" />
    <figcaption>ws11 ping 10.100.0.12</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_24.png" alt="Part_5_24" />
    <figcaption>r2 sudo tcpdump -tn -i enp0s8</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_25.png" alt="Part_5_25" />
    <figcaption>r1 статический маршрут</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_26.png" alt="Part_5_26" />
    <figcaption>r2 статический маршрут</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_27.png" alt="Part_5_27" />
    <figcaption>r1 ip r</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_28.png" alt="Part_5_28" />
    <figcaption>r2 ip r</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_29.png" alt="Part_5_29" />
    <figcaption>ip r list 10.10.0.0/18 и ip r list 0.0.0.0/0</figcaption> 
</figure> 

Для сети 10.10.0.0/18 предпочтение было отдано специфичному маршруту, а не маршруту по умолчанию (0.0.0.0/0), так как в маршрутизации действует принцип «наиболее длинного совпадения префикса» (longest prefix match). Это правило гарантирует выбор более точного пути: маршрут с более детальной маской (большей длиной префикса) всегда приоритетен. Таким образом, маршрут по умолчанию активируется только при отсутствии альтернатив, так как его префикс 0.0.0.0/0 является наименее специфичным.

* Построение списка маршрутизаторов

<figure>
    <img src="./screen/Part_5_30.png" alt="Part_5_30" />
    <figcaption>ws11</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_31.png" alt="Part_5_31" />
    <figcaption>r1</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_32.png" alt="Part_5_32" />
    <figcaption>ws11</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_33.png" alt="Part_5_33" />
    <figcaption>r1</figcaption> 
</figure> 

## Часть 6. Динамическая настройка IP с использованием DHCP

* Для r2 настрой в файле /etc/dhcp/dhcpd.conf конфигурацию службы DHCP:

<figure>
    <img src="./screen/Part_5_34.png" alt="Part_5_34" />
    <figcaption>/etc/dhcp/dhcpd.conf</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_35.png" alt="Part_5_35" />
    <figcaption>/etc/resolv.conf</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_36.png" alt="Part_5_36" />
    <figcaption>ip a</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_37.png" alt="Part_5_37" />
    <figcaption>ping 10.20.0.10</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_38.png" alt="Part_5_38" />
    <figcaption>/etc/netplan/00-installer-config.yaml</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_39.png" alt="Part_5_39" />
    <figcaption>r1 /etc/dhcp/dhcpd.conf</figcaption> 
</figure> 

<figure>
    <img src="./screen/Part_5_40.png" alt="Part_5_40" />
    <figcaption>WS11 ip a после перезагрузки</figcaption> 
</figure> 


<figure>
    <img src="./screen/Part_5_41.png" alt="Part_5_41" />
    <figcaption>ws21 до смены ip</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_42.png" alt="Part_5_42" />
    <figcaption>обновление ip</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_5_43.png" alt="Part_5_43" />
    <figcaption>ws21 после обновления ip</figcaption> 
</figure> 

## Часть 7. НАТ

* В файле /etc/apache2/ports.conf измените строку Listen 80на Listen 0.0.0.0:80on ws22 и r1, т.е. сделайте сервер Apache2 публичным

<figure>
    <img src="./screen/Part_7_1.png" alt="Part_7_1" />
    <figcaption>ws22</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_7_2.png" alt="Part_7_2" />
    <figcaption>r1</figcaption> 
</figure> 


* Запустите веб-сервер Apache с помощью service apache2 startкоманды на ws22 и r1

<figure>
    <img src="./screen/Part_7_3.png" alt="Part_7_3" />
    <figcaption>ws22</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_7_4.png" alt="Part_7_4" />
    <figcaption>r1</figcaption> 
</figure> 


<figure>
    <img src="./screen/Part_7_5.png" alt="Part_7_5" />
    <figcaption>Пинг с ws22 до r1 не удаётся</figcaption> 
</figure> 
<figure>
    <img src="./screen/Part_7_6.png" alt="Part_7_6" />
    <figcaption>Пинг с ws22 до r1 удаётся</figcaption> 
</figure> 
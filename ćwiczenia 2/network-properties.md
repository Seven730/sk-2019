Ustawianie parametrów sieci
---------------------------

![alt text][network]

[network]: ./network.png "Logo Title Text 2"

1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
|   PC 1 | 1 
| IP - address  | 10.7.100.4```/24``` | |
| MASKA  | gumiforest.uek.krakow.pl | |
|   |  | |
| PC 2  | 2 | |
| IP - address  | 10.7.100.5```/24``` | |
| MASKA  | gumiforest.uek.krakow.pl | |

Weryfikacja połączenia

Polecenie
ping 10.7.100.4
ping 10.7.100.5

Efekt
64 bytes from 10.7.100.4: icmp_seq=1 ttl=64 time=0.410 ms
...
64 bytes from 10.7.100.5: icmp_seq=1 ttl=64 time=0.346 ms
...

Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | |
| MASKA  | 255.255.0.0 | |

Weryfikacja połączenia

Polecenie
```
```

Efekt
```
```

Nowa statyczna konfiguracja 

-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  |  | |
| MASKA  |  | |
|   |  | |
| PC 2  |  | |
| IP - address  |  | |
| MASKA  |  | |

Weryfikacja połączenia

Polecenie
```
```

Efekt
```
```

Warto wiedzieć
--------------

-------------------------
| Parametr | wartość | komentarz(opcionalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| | |
| UP -> Wyłączenie interfejsu sieciowego| ifup | |
| DOWN -> Włączenie interfejsu sieciowego| ifdown | |
| Sprawdzenie obecnych parametrów | | |
| lista wszystkich interfejsów | ip a | |
| Które interfejsy jakie porty słuchają | | |

NOTATKI
ip a
ifup enp0s3
ifdown enp0s3
nmcli
sudo
ping ...
yum install git
apt-get
git clone https://github.com/jkanclerz/http-chat
python httpchat.py
curl -d '{"text":"hello"}' https://10.7.100.4:8888/messages
curl -d '{"last_message_id":-1}' https://10.7.100.4:8888/messages
curl -d '{"text":"hello"}' http://10.7.100.4:8888/messages
curl -d '{"last_message_id":-1}' http://10.7.100.4:8888/messages | python -m json.tool
curl -d '{"text":"hello"}' http://10.7.100.4:8888/chat
systemctl stop firewalld


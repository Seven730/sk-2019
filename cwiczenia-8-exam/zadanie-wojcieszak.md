Zadanie 1
---------

![zadanie 1](zadanie-1.svg)

1. Zaprojektuj oraz przygotuj prototyp rozwiązania z wykorzystaniem oprogramowania ``VirtualBox`` lub podobnego. 
Zaproponuj rozwiązanie spełniające poniższe wymagania:
   * Usługodawca zapewnia domunikację z siecią internet poprzez interfejs ``eth0`` ``PC0``
   * Zapewnij komunikację z siecią internet na poziomie ``LAN1`` oraz ``LAN2``
   * Dokonaj takiego podziału sieci o adresie ``172.22.128.0/17`` aby w ``LAN1`` można było zaadresować ``500`` adresów natomiast w LAN2 ``5000`` adresów    
   * Przygotuj dokumentację powyższej architektury w formie graficznej w programie ``DIA``
 
-------------------------------------------------------------------------------------------------------------------------

172.22.128.0/17 - Adres do podziału

Na początku obliczyłem maskę na zasadzie 2 do której da mi więcej od zadanej liczby użytkowników.
Potem za pomocą strony http://jodies.de/ipcalc wykalkulowałem drugi adres.

172.22.160.0/23 - LAN 1

172.22.128.0/19 - LAN 2

Podpiąłem sieci w VirtualBox wzorując się na schemacie tzn
PC1 - LAN1
PC2 - LAN2
PC0 - LAN1 LAN2 NAT

PC0:
Włączyłem PC0, sprawdziłem połączenie z internetem - nie działa.
Sprawdziłem co się dzieje ip a.
Wszedłem w plik interfaces i go edytowałem w nano za pomocą komedy:
nano /etc/network/interfaces

Zmieniłem interfejsy na 

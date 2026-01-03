# Windows Serwer - Konfiguracja DHCP i rezerwacja adresów

## Wymagania wstępne

- Maszyna virtualna z systemem _**Windows Server 2025**_.
- Maszyna virtualna z systemem _**Ubuntu 24.04 Desktop**_.
- Maszyna virtualna z systemem _**Windows 11 Pro**_.

## Treść zadania

- Skonfiguruj ustawienia maszyn virtualnych:

  - _**Windows Server 2025**_:
    - **Karta 2**: `NAT`.
    - **Karta 3**: `Sieć wewnętrzna`.
  - _**Ubuntu 24.04 Server**_:
    - **Karta 1**: `Sieć wewnętrzna`.
  - _**Windows 11 Pro**_:
    - **Karta 1**: `Sieć wewnętrzna`.

- Dokonaj konfiguracji interfejsów sieciowych działających w trybie `Sieć wewnętrzna`.

  | _**Windows Server 2025**_                |                |
  | ---------------------------------------- | -------------- |
  | Adres IP / skrócony adres maski podsieci | `192.168.5.20/24` |

Klienci mają mieć ustawione interfejsy na automatyczny `DHCP`


- Skonfiguruj DHCP
  - Pula: `192.168.5.40` ÷ `192.168.5.60`
  - Maska podsieci klasa _**C**_
  - Zarezerwuj adres `192.168.5.200` dla maszyny z systemem *Windows 11 Pro*
- Przeprowadź test łączności komendą `ping` pomiędzy maszynami.

# Laboratorium 13 – Sekrety w Docker Compose

##  Opis projektu

Projekt realizuje stack LEMP (Linux, Nginx, MySQL, PHP-FPM) z dodatkową usługą phpMyAdmin. Wszystko uruchamiane i zarządzane za pomocą pliku `docker-compose.yml`.

##  Usługi w kontenerach

- **Nginx** (port: `4001`) — serwer HTTP
- **PHP-FPM** — interpreter PHP
- **MySQL 8.3** — baza danych (zainicjalizowana)
- **phpMyAdmin** (port: `6001`) — interfejs webowy do MySQL

## Sekrety

Zmieniono sposób przekazywania danych wrażliwych:

- `MYSQL_ROOT_PASSWORD` → przekazywane jako `db_root_password` z pliku `secrets/db_root_password.txt`
- `MYSQL_PASSWORD` → przekazywane jako `db_password` z pliku `secrets/db_password.txt`

## Uruchomienie

##  Uruchomienie projektu
docker compose up -d

##  Wejście na strony
- http://localhost:4001 → strona PHP
- http://localhost:6001 → phpMyAdmin
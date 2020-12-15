### 1. Ansible

Popraw **wszystkie** błędy w pliku `date-flag-playbook.yml` (poniżej). Jak uruchomić ten plik? (napisz komendę w bash):

```json
---
- host: localhost
  task:
    - name: create date_flagg file
      lineifile:
         creates: yes
       lines: "{{ ansible_date_time.date }}"
dests: /tmp/date_flag
```

### 2. bash

- a) przeiteruj przez linie w pliku `./ttt` i wykonaj na każdej z nich polecenie `echo`
- b) ustaw limit otwartych plików na 1024 w obecnej sesji logowania
- c) Popraw wszystkie błędy w poniższym wywołaniu:

```bash
DOCKER_FLAGS="-ti ubuntu:latest cat /etc/resolf.conv"
docker runn "${DOCKER_FLAGS}"
```

### 3. networking

Rozważ architekturę, w której na serwerze `app01.local` uruchomiony jest Apache Tomcat, który na porcie 8080 wystawia aplikację webową "X". Maszyna `app01.local` nie ma dostępu do Internetu, ale posiada serwer ssh (port 2222). Firewall blokuje wszystkie połączenia przychodzące do `app01.local` oprócz połączeń z serwera `jump.local` skierowanych na port 2222. **W jaki sposób otworzysz aplikację "X" w przeglądarce na swoim laptopie** biorąc pod uwagę fakt, że możesz połączyć się do `root@jump.local` za pomocą ssh, a użytkownik root z `jump.local` ma dodany klucz ssh na app01.local?

### 4. CI/CD

Napisz plik `.gitlab-ci.yml` lub `bitbucket-pipelines.yml`, który wykorzystywałby Mavena do zbudowania kodu i wysłania paczki `war` do Artifactory, zakładając, że `pom.xml` jest odpowiednio skonfigurowany. Opcjonalnie, jeśli nie jesteś zaznajomiony z Mavenem może to być Gradle i Artifactory, albo nawet Python i PyPi lub Composer i Satis.

### 5. Architektura

Zaprojektuj infrastrukturę dla aplikacji webowej na AWS lub Azure, biorąc pod uwagę następujące warunki:

- frontend to aplikacja SPA w Angular
- bakcend to REST API w Python uruchomione na dockerze 
- backend musi być samo-skalowalny, zależnie od liczby odwiedzających
- aplikacja korzysta z bazy danych Mysql
- aplikacja korzysta z Redis do zarządzania sesją
- aplikacja posiada funkcjonalność uploadowania plików przez użytkowników. Pliki te muszą być następnie dostępne dla serwerów backendowych

Forma odpowiedzi dowolna.

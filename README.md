# Medfile API Index

Medfile oferuje różne interfejsy do integracji zewnętrznych aplikacji z Medfile. Poniżej znajduje się spis zastosowań różnych interfejsów i odnośniki do najważniejszych informacji.

## Spis treści

- [Medfile API Index](#medfile-api-index)
  - [Spis treści](#spis-treści)
  - [Medfile Widget API](#medfile-widget-api)
  - [Medfile Auth Service API](#medfile-auth-service-api)
  - [Medfile API (FHIR)](#medfile-api-fhir)
  - [Medfile Services API](#medfile-services-api)

---

## Medfile Widget API

Dla klientów budujących własny interfejs do rejestracji pacjentów stworzyliśmy dedykowany interfejs REST API o nazwie Medfile Widget API tzw. API do rejestracji online.
Usługa umożliwia wyszukanie m.in. specjalisty, usługi oraz terminu. Następnie dedykowany endpoint umożliwia finalizację rejestracji bez wychodzenia z Państwa aplikacji.

**Kiedy ta usługa jest zalecana?**
- Gdy klient buduje własny interfejs do rejestracji pacjentów i chce osadzić formularz rejestracji w swojej aplikacji.
- Gdy klient chce umożliwić pacjentom rezerwację wizyt online bez przekierowywania ich do aplikacji Medfile.

**Linki:**
- Opis funkcji: https://www.medfile.pl/api-do-rejestracji-online
- Interaktywna dokumentacja: https://wapi.medfile.pl/docs
- Przypadki użycia i wskazówki implementacyjne: https://github.com/biostatteam/medfile-widget-api

---

## Medfile Auth Service API

Usługa umożliwia autentykację użytkowników w zewnętrznym oprogramowaniu i autoryzację w aplikacji Medfile poprzez przekazanie tokenu JWT.

**Kiedy ta usługa jest zalecana?**
- Gdy klient posiada własny system CRM lub inny do codziennej pracy swoich lekarzy lub użytkowników. Chciałby dla każdego zalogowanego u siebie użytkownika łatwo otwierać aplikację Medfile bez konieczności dodatkowego logowania się. Możliwe, że klient chciałby otworzyć aplikację Medfile wewnątrz swojego programu CRM — może to zrobić dodatkowo instalując Medfile w kontenerze IFRAME.
- Gdy klient posiada własny system autentykacji i nie chce używać formularza logowania Medfile — np. posiada własny serwer LDAP lub własną aplikację CRM.

**Linki:**
- Dokumentacja: w budowie
- Przykład zastosowania w Medfile API (FHIR): https://github.com/biostatteam/medfile-api/blob/master/docs/Specyfikacja-Medfile-Auth-Service.md

---

## Medfile API (FHIR)

Interfejs umożliwia zarządzanie kalendarzem, tworzeniem kartotek pacjentów, dodawanie załączników oraz rejestrację subskrypcji na wybrane zdarzenia — np. gdy wizyta zostanie anulowana.

**Kiedy ta usługa jest zalecana?**
- Gdy klient potrzebuje zintegrować swój własny system CRM lub inny z Medfile — np. chciałby synchronizować wizyty i kartoteki pacjentów ze swoim systemem w czasie prawie rzeczywistym.
- Gdy klient potrzebuje zarządzać swoimi pracownikami zdalnie bez konieczności używania aplikacji Medfile.
- Gdy klient potrzebuje pobierać załączniki pacjentów z Medfile lub dodawać z innego systemu załączniki pacjentów do kartoteki pacjentów w Medfile.
- Gdy klient potrzebuje otrzymywać w czasie bliskim rzeczywistemu informacje o nowych wizytach, nowych pacjentach i innych zdarzeniach.
- Gdy klient posiada własny portal pacjenta i chce pokazywać w nim wizyty pacjentów oraz ich załączniki.

**Linki:**
- Dokumentacja: https://github.com/biostatteam/medfile-api
- Aplikacja demonstracyjna: https://github.com/biostatteam/medfile-api/blob/master/demo/README.md

---

## Medfile Services API

Dla klientów, którzy nie korzystają z aplikacji Medfile App (https://app.medfile.pl), ale chcą zaimplementować w swoim programie integrację z e-receptą lub innymi usługami szyny P1 i nie tylko, oferujemy dedykowany interfejs Medfile Services API.

**Kiedy ta usługa jest zalecana?**
- Gdy klient chce wystawiać e-recepty lub e-ZLA bezpośrednio ze swojego oprogramowania, bez konieczności korzystania z aplikacji Medfile App.
- Gdy klient potrzebuje integracji z usługami szyny P1 (np. weryfikacja uprawnień pacjenta, e-skierowania) w ramach własnego systemu.

**Linki:**
- Opis funkcji: https://www.medfile.pl/api-erecepta-ezla
- Dokumentacja: https://github.com/biostatteam/medfile-services-api-wiki

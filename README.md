# Medfile API Index

Medfile oferuje różne interfejsy do integracji zewnętrznych aplikacji z Medfile. Poniżej znajduje się spis zastosowań różnych interfejsów i odnośniki do najważniejszych informacji.

## Medfile Widget API tzw. API do rejestracji online

Dla klientów budujących własny interfejs do rejestracji pacjentów stworzyliśmy dedykowany interejs REST API o nazwie Medfile Widget API tzw. API do rejestracji online.
Usługa umożliwia wyszukanie m.in. specjalisty, usługi oraz terminu. Następnie dedykowany endpoint umożliwia finalizację rejestracji bez wychodzenia z Państwa aplikacji.

- Opis funkcji https://www.medfile.pl/api-do-rejestracji-online
- Interaktywna dokumentacja: https://wapi.medfile.pl/docs
- Przypadki użycia i wskazówki implementacyjne: w budowie

## Medfile Services API

Dla klientów którzy nie korzystają z aplikacji Medfile App (https://app.medfile.pl) ale chcą zaimplementować w swoim programie integrację z e-receptą lub innymi usługami szyny P1 i nie tylko oferujemy dedykowany interfejs Medfile Services API.

Dokumentacja: https://github.com/biostatteam/medfile-services-api-wiki

## Medfile Auth Service API

Usługa umożliwia autentykację użytkowników w zewnętrznym oprogramowaniu i autoryzację w aplikacji Medfile poprzez przekazanie tokenu JWT. 

**Kiedy ta usługa jest zalecana?**
- Gdy klient posiada własny system CRM lub inny do codziennej pracy swoich lekarzy lub użytkowników. Chciałby dla każdego zalogowanego u siebie użytkownika łatwo otwierać aplikację Medfile bez konieczności dodatkowego logowania się. Możliwe, że klient chciałby otworzyć aplikację Medfile wewnątrz swojego programu CRM, może to zrobić dodatkowo instalując Medfile w kontenerze IFRAME.
- Klient posiada własny system autentykacji i nie chce używać naszego formularza logowania - np. posiada własny serwer LDAP lub własną aplikację CRM.

Dokumentacja: w trakcie

## Medfile API (FHIR)

Interfejs umożliwia zarządzanie kalendarzem, tworzeniem kartotek pacjentów, dodawanie załączników oraz rejestrację subskrypcji na wybrane zdarzenia np. gdy wizyta zostania anulowana.

**Kiedy ta usługa jest wykorzystywana?**
- Gdy klient potrzebuje zintegrować swój własny system CRM lub inny z Medfile. Np. chciałby synchronizować wizyty i kartoteki pacjentów ze swoim systemem w czasie prawie rzeczywistym.
- Gdy klient potrzebuje zarządzać swoimi pracownikami zdalnie bez konieczności używania aplikacji Medfile.
- Gdy klient potrzebuje pobierać załączniki pacjentów z Medfile lub dodawać z innego systemu załączniki pacjentów do kartoteki pacjentów w Medfile.
- Gdy klient potrzebuje otrzymywać w czasie bliskim rzeczywistemu informacje o nowych wizytach, nowych pacjentach i innych zdarzeniach.
- Gdy klient posiada własny portal pacjenta i chce pokazywać w nim wizyty pacjentów oraz ich załączniki.

Dokumentacja: w trakcie

# FlightReservationApp


## Role i posiadane funkcje:
Administrator:
- możliwość przejrzenia listy zarejestrowanych użytkowników wraz z posiadaną przez nich rolą i filtrowania listy użytkowników względem ich roli. 
- możliwość tworzenia kont użytkowników przypisując im odpowiednią role: rezerwujący, manager lotów, administrator. 
- możliwość przeglądania dostępnych lotów i ich filtrowania. 

Manager lotów:
- możliwość przeglądania wszystkich dostępnych lotów i ich filtrownia. 
- możliwość dodawania lotu jego edycji oraz zmiany statusu
- wgląd do rezerwacji dokonanych w systemie. 
- anulowanie rezerwacje użytkowników. 

Gość:
- możliwość zalogowania się do systemu lub utworzenia konta i jego aktywacji. 
- otrzymanie e-mail z linkiem do aktywacji utworzonego konta. 
- możliwość przeglądania lotów i ich filtracji. 

Rezerwujący: 
- możliwość przeglądania lotów i ich filtracji. 
- możliwość złożenia rezerwacji. 
- możliwość wybrania miejsca w samolocie podczas składania rezerwacji. 
- możliwość przeglądania historii moich rezerwacji oraz ich anulacji. 
- otrzymanie e-maila z potwierdzeniem rezerwacji. 

## Wymagania
Należy posiadać: Java 11, Spring Boot, Hibernate i JPA, Środowisko IntelliJ IDEA, PostgreSQL 13.3 wraz z pgAdmin4

## Instrukcja uruchomienia
Aplikacja działa tylko w środowisku lokalnym, więc w celu jej uruchomienia należy pobrać kody projektu. Do uruchomienia wersji serwerowej aplikacji potrzebna będzie Java 11, PostgreSQL w wersji 13 oraz środowisko programistyczne
przykładowo Intellij Idea. Po zainstalowaniu wszystkich wspomnianych programów w środowisku programistycznym należy otworzyć pobrany projekt z repozytorium Git. Następnie należy wejść do katalogu resources w module main i wybrać w nim
application.properties. W tym pliku znajduje się nazwa schematu, nazwa użytkownika i hasło do bazy danych. Posiadając te dane można otworzyć PostreSQL i lokalnie utworzyć użytkowania o takiej nazwie i haśle oraz schemat.
Użytkownikowi należy jeszcze nadać uprawnienia do dodawania, przeglądania oraz edycji. Po tym kroku można już spokojnie uruchomić projekt i wszystkie tabele powinny utworzyć się same. W związku z tym, że bez utworzonego konta o roli
administratora jest możliwość tworzenia kont tylko z rolą rezerwującego, konieczna będzie chwilowa zmiana w klasie SecurityConfig i RegisterController. Posiadając działającą część serwerową należy jeszcze uruchomić część kliencką. Udostępnioną w osobny repozytorium.

## Swagger
Do aplikacji dodany jest swagger
http://localhost:8081/swagger-ui.html?fbclid=IwAR0amajFCkBMO6k2lhEq9TgglEkkAEDiZHYj8YeX-OZ4KuPoMZ_SJO-Z7og#/

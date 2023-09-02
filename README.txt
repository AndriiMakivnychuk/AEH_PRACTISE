Więc najpierw opowiem pokrótce, jak wykonałem projekt, a poniżej opiszę instrukcje, jak uruchomić witrynę.
Ponieważ jestem programistą JavaScript, zdecydowałem się napisać API w nodeJS, aby nie komplikować sobie życia.
Zacząłem oczywiście od HTML i CSS wykorzystałem również GULP builder aby wygodniej się pracowało, podłączyłem pluginy
do slidera wykorzystałem swiper.js. Następnie skompilowałem i skompresowałem cały layout i przeniosłem się na stronę serwera.
Całą logikę umieściłem w pliku logic.js nie było sensu komplikować, gdyż była ona niezbędna do autoryzacji i nawigacji na stronach.

INSTRUKCJA URUCHOMIENIA STRONY
1. Połącz się z bazą danych mySql, jest wiele sposobów ja zawsze używam panelu "xampp". 
2. Po połączeniu utworzyć bazę danych pod nazwą "nodejs", generalnie można ją nazwać jak się chce,
ale jeśli nie chce się nic zmieniać w plikach skryptu, to tak ją nazwać, następnie utworzyć tabelę "loginuser" tam
będą trzy kolumny user_id, user_name, user_password.Utwórz nowy wiersz w bazie danych, który będzie naszym użytkownikiem,
tj. wpisz nazwę użytkownika i hasło.
3.Po wejściu do folderu projektu będziesz musiał zainstalować rozszerzenia, aby wszystko działało.
W terminalu wpisz następujące polecenia
"npm install mysql"
"npm install express"
"npm isntall body-parser"
4.Przejdź do mojego projektu i uruchom plik logic.js, jeśli utworzyłeś nowego użytkownika podczas łączenia się z bazą danych,
będziesz musiał zmienić nazwę i hasło w tym miejscu w logic.js.
const connection = mysql.createConnection({
  host: "localhost",
  user: "root",
  password: "",
  database: "nodejs"
});
Wpisz nazwę użytkownika i hasło, a następnie uruchom plik. Jeśli wszystko pójdzie dobrze, terminal wyświetli komunikat "connected".
5.W przeglądarce w pasku adresu wpisz "localhost:4000", jeśli zrobiłeś wszystko zgodnie z instrukcjami,
powinieneś zobaczyć stronę autoryzacji.


Jeśli masz jakieś pytania lub nie możesz uruchomić usługi, skontaktuj się ze mną

mój telefon: 793796469 albo napisz ma meila
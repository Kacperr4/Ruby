//puts "Podaj nazwę przedmiotu:"
//przedmiot = gets.chomp.downcase
//gets – Pobiera tekst wpisany przez użytkownika.
//chomp – Usuwa znak nowej linii (\n), który gets automatycznie dodaje.
//downcase – Zamienia wszystkie litery na małe, aby użytkownik mógł wpisać np. "Matematyka", a program nadal to rozpoznał jako "matematyka".
//
//2. Pobieranie liczb i ich konwersja
//Domyślnie gets zwraca tekst (String), więc jeśli użytkownik wpisuje liczbę, trzeba ją przekonwertować:
//
//puts "Podaj liczbę:"
//liczba = gets.chomp.to_i  # Konwersja na liczbę całkowitą
//puts "Podwojona wartość: #{liczba * 2}"
//Podobnie można konwertować na liczby zmiennoprzecinkowe:
//waga = gets.chomp.to_f  # Konwersja na float

3. Pobieranie wielu wartości na raz
Jeśli użytkownik wpisuje kilka wartości oddzielonych spacją, można je podzielić na tablicę:

puts "Podaj kilka liczb oddzielonych spacją:"
liczby = gets.chomp.split.map(&:to_i)  # Tworzymy tablicę i konwertujemy na liczby
puts "Suma liczb: #{liczby.sum}"


4. Pobieranie argumentów z linii poleceń
Można przekazać dane do programu przez argumenty w wierszu poleceń, korzystając z ARGV:

puts "Podano argumenty: #{ARGV.inspect}"
Jeśli uruchomimy skrypt tak:

ruby program.rb 3 7 9
To ARGV będzie zawierać ["3", "7", "9"], ale nadal jako stringi. Można je przekonwertować:

liczby = ARGV.map(&:to_i)
puts "Suma: #{liczby.sum}"


6. Wczytywanie całych linii tekstu
Jeśli chcesz wczytać wiele linii naraz, możesz użyć while gets:

puts "Wpisuj linie, zakończ Ctrl+D (Linux) lub Ctrl+Z (Windows):"
linijki = []
while (linia = gets)
  linijki << linia.chomp
end
puts "Otrzymano:"
puts linijki.join("\n")

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

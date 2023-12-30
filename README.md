# Konwolucyjne Sieci Neuronowe (CNN) dla Klasyfikacji Obrazów

## Opis

Ten projekt zawiera implementację konwolucyjnych sieci neuronowych (CNN) w Pythonie przy użyciu biblioteki Keras. Kod ten pozwala na klasyfikację obrazów na zestawach danych MNIST i CIFAR-10, eksperymentując z różnymi architekturami sieci.

## Wymagania

- Python 3.x
- Biblioteki: Keras, NumPy, Matplotlib, SciKit-Learn

## Użycie

1. Pobierz pliki z repozytorium.
2. Uruchom kod w środowisku obsługującym język Python.

## Instrukcje

1. **Zadanie 7.2 - Znalezienie optymalnej liczby warstw**

   - W pliku `mnist_cnn.py` znajdziesz kod do znalezienia optymalnej liczby warstw za pomocą GridSearchCV dla zestawu danych MNIST.
   - Wykresy i wnioski z eksperymentów są opisane w kodzie.

2. **Zadanie 7.3 - Wpływ warstw głosujących**

   - `mnist_cnn.py` również zawiera eksperymenty dotyczące warstw MaxPooling i AveragePooling oraz ich wpływu na sieci CNN.
   - Wnioski i wykresy są zawarte w kodzie wraz z analizą.

3. **Zadanie 7.4 - Klasyfikacja CIFAR-10**
   - `cifar10_cnn.py` obejmuje kod do klasyfikacji obrazów z zestawu danych CIFAR-10.
   - Przeprowadzono eksperymenty w celu znalezienia optymalnej liczby warstw, wygenerowania macierzy pomyłek i analizy wyników.

## Uwaga dot. KerasClassifier

- W trakcie implementacji tego projektu użyto KerasClassifier, który obecnie jest przestarzały. Zalecane jest przejście na Sci-Keras (https://github.com/adriangb/scikeras) zgodnie z instrukcjami dostępnymi pod adresem https://www.adriangb.com/scikeras/stable/migration.html.

## Wyniki

- Znaleziono optymalną liczbę warstw dla zbioru danych MNIST (5 warstw).
- Warstwy pooling wpływają na stabilność sieci i zjawisko przetrenowania. AvgPooling wydaje się być lepszy niż MaxPooling.
- Dla CIFAR-10 optymalna liczba warstw to 5, na podstawie analizy eksperymentalnej.

## Macierz Pomyłek - CIFAR-10

```
[[696 26 67 28 27 6 16 14 74 46]
[ 39 738 11 22 5 7 10 10 39 119]
[107 5 452 101 100 67 93 44 18 13]
[ 34 20 106 455 67 153 95 44 17 9]
[ 27 4 98 90 518 44 102 102 10 5]
[ 17 6 101 239 57 430 44 84 11 11]
[ 10 6 73 81 53 20 726 20 7 4]
[ 25 6 59 71 68 67 19 667 0 18]
[171 42 13 24 16
```

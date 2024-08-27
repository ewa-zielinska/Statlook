1. Po wprowadzeniu poprawnych danych do Formularza zgłaszania naruszeń i kliknięciu przycisku 'Powrót' lub w logo 'Statlook' - bez żadnej informacji użytkownik zostaje przekierowany na stronę główną, a wprowadzone dane zostają usunięte.

   __Przypadek testowy:__
   - Wejdź na stronę [https://demo.statlook.com/whistleblower/issue/new](https://demo.statlook.com/whistleblower/issue/new)
   - Uzupełnij formularz danymi, które są obligatoryjne
   - Kliknij przycisk 'Powrót' na dole strony / Kliknij logo 'Statlook' w prawym lewym rogu strony

   __Rezultat:__
   - Użytkownik zostaje przekierowany na stronę główną, a wprowadzone dane zostały utracone

   __Oczekiwany rezultat:__
   - W takim przypadku dobrym pomysłem byłoby wyświetlenie okna modalnego z alertem: "Zostaniesz przekierowany do strony głównej, a wprowadzone przez Ciebie dane zostaną usunięte. Potwierdzasz wykonanie operacji?" z opcją wyboru 'TAK' lub 'NIE'

---

2. Na stronie głównej mamy informację, że:

   > Poprawne zgłoszenie powinno:
   > - Zawierać kategorię nieprawidłowości, którą chcesz zgłosić (jeżeli nie masz pewności, wybierz „inne”)

   Obecnie można przesłać zgłoszenie, gdzie w comboboxie jest zaznaczona opcja '(Nie określono)'

   __Przypadek testowy:__
   - Wejdź na stronę [https://demo.statlook.com/whistleblower/issue/new](https://demo.statlook.com/whistleblower/issue/new)
   - W comboboxie 'Jakiego obszaru dotyczy zgłoszenie?' - nie zmieniaj nic, pozostaw wartość '(Nie określono)'
   - Uzupełnij pozostałe pola, które są obligatoryjne
   - Kliknij przycisk 'Wyślij zgłoszenie'

   __Rezultat:__
   - Zgłoszenie zostało przesłane

   __Oczekiwany rezultat:__
   - W takim przypadku pole powinno podświetlić się na czerwono z informacją, że wybór opcji z listy jest obligatoryjny

---

3. Po zmianie widoku na 'LARGE' nazwy obszarów w rozwijanej liście w comboboxie są ucinane.

   __Przypadek testowy:__
   - Wejdź na stronę [https://demo.statlook.com/whistleblower/issue/new](https://demo.statlook.com/whistleblower/issue/new)
   - W prawym górnym rogu na głównej belce zmień opcję widoku na 'LARGE'
   ![image](https://github.com/user-attachments/assets/5b2094aa-055c-4804-a837-27365c7d28d5)
   - Rozwiń listę obszarów

   __Rezultat:__
   - Nazwy obszarów są przycięte w pionie
![image](https://github.com/user-attachments/assets/7a6a20e9-0afe-411d-af32-fb9e01d2bcda)

   __Oczekiwany rezultat:__
   - Nazwy obszarów powinny wyświetlać się poprawnie w tym trybie

---

4. Dodając komentarz do zgłoszenia, który zawiera więcej niż 1000 znaków pojawia się informacja o niepoprawnej długości, jednak taki komentarz można dodać, a znaki przekraczające dozwoloną długość są ucinane. W takim przypadku nie powinno być możliwości dodania komentarza > 10000 znaków.

   __Dane wejściowe:__ Poprawnie utworzone zgłoszenie

   __Przypadek testowy:__
   - Wejdź na stronę [https://demo.statlook.com/whistleblower/issue/check](https://demo.statlook.com/whistleblower/issue/check)
   - Wprowadź poprawny numer sprawy oraz Kod weryfikacyjny
   - Przejdź do zakładki 'Komentarze'
   - Wpisz wiadomość dłuższą niż 10000 znaków
   - Kliknij przycisk 'Dodaj komentarz'

   __Rezultat:__
   - Komentarz został dodany.

   __Oczekiwany rezultat:__
   - Komentarz nie powinien zostać dodany

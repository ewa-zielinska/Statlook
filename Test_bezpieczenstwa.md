1. Bezpieczeństwo transmisji danych

__Protokół HTTPS:__

Adres URL strony do przesyłania zgłoszeń zaczyna się od "https://" - co oznacza, że połączenie jest szyfrowane.

__Certyfikat SSL:__

Certyfikat SSL został wydany przez jednego z uznawanych dostawców certyfikatów Go Daddy i jest aktualny. 

![image](https://github.com/user-attachments/assets/1e726ecd-8bbe-4793-94bb-4a3861f3c8e9)


Test na stronie https://www.whynopadlock.com/ dla podanego adresu URL został zaliczony tzn. że połączenie SSL zostało pomyślnie ustanowione i jest uznawane za bezpieczne. Jenak należy zwrócić uwagę na fakt, że serwer obsługuje protokół TLSv1, który jest już przestarzały i niezalecany do użytku ze względu na luki bezpieczeństwa. Być może należałoby zaktualizować konfigurację serwera, tak aby zapewnić lepsze bezpieczeństwo. 

![image](https://github.com/user-attachments/assets/90152b65-4c05-454b-91e7-4841cb0e9d70)

2. Walidacja i Sanityzacja

__Walidacja__

W polach formularza nie ma walidacji jeśli chodzi o rodzaj znaków. Pola formularza przyjmują wszystkie znaki. Walidacja jest na ilość znaków. Jeśli jakieś pole ma więcej niż 10000 znaków nie da się przesłać formularza. Dodatkowo pole 'Opis naruszenia' musi zawierać conajmniej 1 znak. 

__Sanityzacja__

Znaki specjalne są wyświetlane poprawnie, dane w formacie HTML, JS,  JSON, XML są wyświetlane jako teskt, białe znaki są usuwane.

3. Bezpieczeństwo informacji w panelu administracyjnym

Dane w formularzu przesyłane są plain tekstem. 

![image](https://github.com/user-attachments/assets/8be531a3-0e1c-487f-9c67-ce836e84c809)

## Diagram przepływu aplikacji do planowania posiłków
Architektura interfejsu użytkownika

```mermaid
flowchart TD
    A[Start Aplikacji] --> B[Ekran Główny<br/>Przegląd tygodnia]
    B --> C{Wybór Akcji}
    
    C --> D[Zarządzaj Przepisami]
    C --> E[Zaplanuj Posiłek]
    C --> F[Generuj Listę Zakupów]
    
    D --> D1[Dodaj Przepis]
    D --> D2[Edytuj Przepis]
    D --> D3[Usuń Przepis]
    
    E --> E1[Przeciągnij przepis<br/>na dzień/posiłek]
    
    F --> F1[Automatycznie zsumuj składniki]
    F1 --> F2[Edytuj listę<br/>odhacz kupione produkty]
```

## Objaśnienie diagramu:
  * Start Aplikacji: Użytkownik uruchamia aplikację.
  * Ekran Główny: Wyświetla plan posiłków na bieżący tydzień.
  * Wybór Akcji: Użytkownik wybiera, co chce zrobić. Są trzy główne opcje:
    - Zarządzaj Przepisami: Przejście do bazy przepisów w celu dodania nowego, edycji lub usunięcia istniejącego.
    - Zaplanuj Posiłek: Przeciąganie i upuszczanie przepisów z bazy na konkretny dzień i posiłek (śniadanie, obiad, kolacja) w kalendarzu.
    - Generuj Listę Zakupów: Aplikacja automatycznie zbiera wszystkie składniki z zaplanowanych na dany tydzień posiłków, tworząc kompletną listę. Użytkownik może ją ręcznie edytować, odhaczając kupione produkty.

# movie-buster

## ERD

```mermaid
erDiagram
    MOVIES ||--o{ TICKETS : allows
    MOVIES {
        int Id PK
        string Title
        string MovieGenreId FK
    }
    MOVIES }o--|| MOVIEGENRES : have
    MOVIEGENRES {
        int Id PK
        string Title
        int AgeLimit
    }
    CUSTOMERS ||--o{ TICKETS : have
    TICKETS {
        int Id PK
        string TicketTypeId FK
        string CustomerId FK
        string MovieId FK
    }
    TICKETTYPES {
        int TicketTypeId PK
        int Price
        string Title
    }
    TICKETS }o--|| TICKETTYPES : have
    CUSTOMERS {
        string Id PK
        string FirstName
        string LastName
        int Age
    }
```
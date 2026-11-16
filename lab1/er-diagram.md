```mermaid
erDiagram
    BOOK {
        string title
        int year
        string isbn
    }
    COPY {
        string inventory_number
    }
    AUTHOR {
        string name
        string country
    }
    READER {
        string name
        string phone
        date registration_date
    }
    LOAN {
        date issue_date
        date planned_return_date
        date actual_return_date
    }

    BOOK }o--o{ AUTHOR : "написана"
    BOOK ||--o{ COPY : "має примірники"
    COPY ||--o{ LOAN : "видається"
    READER ||--o{ LOAN : "має"
```
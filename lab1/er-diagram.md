```mermaid
erDiagram
    BOOK {
        string title
        int year
        string isbn
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
    READER ||--o{ LOAN : "має"
    BOOK ||--o{ LOAN : "видається"
```
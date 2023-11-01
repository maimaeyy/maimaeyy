erDiagram
    Member ||--o{ BorrowingTransaction : "Borrows"
    BorrowingTransaction }o--|| Book : "Contains"
    BorrowingTransaction ||--o{ ConditionScan : "Has"
    BorrowingTransaction ||--o{ Fine : "Incur"
    Member {
        string MemberID (PK)
        string FirstName
        string LastName
        string BiometricData
    }
    BorrowingTransaction {
        string TransactionID (PK)
        string BorrowDate
        string ReturnDate
        string ActualReturnDate
    }
    Book {
        string ISBN (PK)
        string Title
        string Author
        string Genre
        int TotalCopies
        int AvailableCopies
    }
    ConditionScan {
        string ScanID (PK)
        string ScanDate
        string ScanResult
    }
    Fine {
        string FineID (PK)
        string FineAmount
        string PaidStatus
    }

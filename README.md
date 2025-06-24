# SQL_intern_task1
This project involves creating three core tables to manage a library database: writers, novel, and borrows. It also implements sequences and triggers to automate primary key generation for each table.
### Tables Created:
### writers
Stores author information with fields:
WriterID (Primary Key)
Name
Nationality
The WriterID is automatically generated using a sequence (writer_seq) and a trigger (trg_writers_id).
### novel
Contains details of novels, including:
NovelID (Primary Key)
Title
Genre
WriterID (Foreign Key referencing writers)
The NovelID is auto-incremented by sequence novel_seq and trigger trg_novel_id.
### borrows
Tracks borrowing records with:
BorrowID (Primary Key)
NovelID (Foreign Key referencing novel)
BorrowerName
BorrowDate
ReturnDate
The BorrowID is generated automatically using sequence borrow_sequence and trigger trg_borrow_id.
### Key Features:
### Sequences: Created for each table to provide unique incremental IDs.

### Triggers: Defined before insert operations to assign the next sequence value to the primary key fields automatically, ensuring consistency and avoiding manual ID management.
### Referential Integrity: Foreign key constraints maintain relational links between novels and their writers, and borrow records with novels.

Sample Data: Initial writers were inserted manually with explicit IDs.

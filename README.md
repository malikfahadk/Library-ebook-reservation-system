![Fahad](https://github.com/user-attachments/assets/acdaf7de-2dd5-439a-8360-6519f256cf55)# Library-ebook-reservation-system
📚 Library E-Book Lending &amp; Reservation System 📖 Welcome to the Library E-Book Lending and Reservation System – a powerful and user-friendly platform designed to modernize and streamline the way libraries manage e-book borrowing and reservations. 
Here's the text version of the **ERD (Entity-Relationship Diagram)** from your image for the **Library E-Book Lending & Reservation System**:

Here's the text version of the **ERD (Entity-Relationship Diagram)** from your image for the **Library E-Book Lending & Reservation System**:

---

### 📦 Tables and Their Fields:

#### **Users**

* UserID (PK)
* Username (varchar(50))
* PasswordHash (varchar(255))

#### **Roles**

* RoleID (PK)
* RoleName (varchar(50))

#### **UserRoles**

* UserID (FK to Users)
* RoleID (FK to Roles)

#### **Members**

* MemberID (PK)
* UserID (FK to Users)
* JoinDate (date)

#### **Staff**

* StaffID (PK)
* UserID (FK to Users)
* Position (varchar(50))

#### **Authors**

* AuthorID (PK)
* FirstName (varchar(50))
* LastName (varchar(50))

#### **Publishers**

* PublisherID (PK)
* Name (varchar(100))
* Email (varchar(100))

#### **Books**

* BookID (PK)
* Title (varchar(255))
* CategoryID (FK to Categories)

#### **Categories**

* CategoryID (PK)
* Name (varchar(100))
* Description (varchar(255))

#### **BookAuthors**

* BookID (FK to Books)
* AuthorID (FK to Authors)

#### **BookPublisher**

* BookID (FK to Books)
* PublisherID (FK to Publishers)

#### **BookCopies**

* CopyID (PK)
* BookID (FK to Books)
* Format (varchar(50))

#### **BookFormats**

* CopyID (FK to BookCopies)
* FormatID (FK to Formats)

#### **Formats**

* FormatID (PK)
* Name (varchar(50))

#### **Reservations**

* ReservationID (PK)
* MemberID (FK to Members)
* BookID (FK to Books)

#### **ReservationStatus**

* ReservationID (FK to Reservations)
* Status (varchar(50))
* ExpiryDate (date)

#### **Lending**

* LendingID (PK)
* MemberID (FK to Members)
* CopyID (FK to BookCopies)

#### **LendingStatus**

* LendingID (FK to Lending)
* DueDate (date)
* ReturnDate (date)

#### **Reviews**

* ReviewID (PK)
* BookID (FK to Books)
* MemberID (FK to Members)

#### **Ratings**

* RatingID (PK)
* BookID (FK to Books)
* Score (int)

#### **Fines**

* FineID (PK)
* MemberID (FK to Members)
* Amount (decimal(6,2))

#### **FinePayments**

* PaymentID (PK)
* FineID (FK to Fines)
* PaymentDate (date)

#### **Notifications**

* NotificationID (PK)
* UserID (FK to Users)
* Message (varchar(255))

#### **Logs**

* LogID (PK)
* UserID (FK to Users)
* Action (varchar(100))

#### **Devices**

* DeviceID (PK)
* UserID (FK to Users)
* DeviceType (varchar(50))

---

Let me know if you'd like this converted into SQL schema code or a markdown ERD summary for your GitHub README!




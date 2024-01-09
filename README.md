## Book Service API

### Overview

This project is a Python-based Book Service API designed for a Python/ML position. The Book Service API manages entities such as Books, Authors, and Clients, providing various API methods for tasks like adding/editing books, retrieving book lists, managing authors and clients, and handling book borrowing.

### Entities

#### Books
- **Book Title**
- **Author** (Additional attributes can be added as needed)

#### Authors
- **Full Name** (Additional attributes can be added as needed)

#### Client
- **Full Name** (Additional attributes can be added as needed)

### API Methods

1. **Add a Book**
2. **Edit Book**
   - Edit the book's title and author.
3. **Retrieve Books**
   - Retrieve a list of books with filtering options for:
     - The first letter of the book's title.
     - Author.
4. **Add Multiple Books by the Same Author**
5. **Add an Author**
6. **Create a Client**
7. **Retrieve Borrowed Books**
   - Retrieve a list of books borrowed by the client.
8. **Link/Unlink a Client to/from a Book**
   - Link a client to a book (client borrowed the book).
   - Unlink a client from a book (client returned the book).

### Considerations

- Authors stored in a separate PostgreSQL database table.
- API secured using an access token (Bearer authentication).
  - Token list can be static.
- Retrieve books borrowed by the client based on the access token.
  - Client identification based on the provided access token.
- Entire infrastructure deployed in Docker.

### Technologies

- **postgreSQL**
- **fastapi**
- **docker**

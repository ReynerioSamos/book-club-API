Test #3
Due: November 22, 2024
To be done individually.


1. Implement a Book Club Management API. We don't have book clubs in Belize but essentially what a 
   book club brings people together to talk about/discuss specific books that they have read.
   
   Your API should be able to track:
   
    - Books { id, title author(s) - handle multiple authors, ISBN, publication date, Genre, Description. Average rating }
    - Reading lists { id, name, description, created by, books, status (currently reading/completed)
    - Book Reviews { id, book id, user id, rating, the actual review of the book, review date }
    - Users {id, username, email, reading lists, reviews }
   
   
2. Implement the following endpoints:


Books
=====

-[x] GET    /api/v1/books              # List all books with pagination
-[x] GET    /api/v1/books/{id}         # Get book details
-[x] POST   /api/v1/books              # Add new book
-[x] PUT    /api/v1/books/{id}         # Update book details
-[x] DELETE /api/v1/books/{id}         # Delete book
-[x] GET    /api/v1/books/search       # Search books by title/author/genre


Reading Lists
=============

[x] GET    /api/v1/lists              # Get all reading lists
[x] GET    /api/v1/lists/{id}         # Get specific reading list
[x] POST   /api/v1/lists              # Create new reading list
[x] PUT    /api/v1/lists/{id}         # Update reading list
[x] DELETE /api/v1/lists/{id}         # Delete reading list
[x] POST   /api/v1/lists/{id}/books   # Add book to reading list
[x] DELETE /api/v1/lists/{id}/books   # Remove book from reading list


Reviews
=======

[x] GET    /api/v1/books/{id}/reviews # Get all reviews for a book
[x] POST   /api/v1/books/{id}/reviews # Add new review
[x] PUT    /api/v1/reviews/{id}       # Update review
[x] DELETE /api/v1/reviews/{id}       # Delete review


Users
======

[x] GET    /api/v1/users/{id}         # Get user profile
[x] GET    /api/v1/users/{id}/lists   # Get user's reading lists
[x] GET    /api/v1/users/{id}/reviews # Get user's reviews



Ensure that:

[x] 1. You activate users via email
[x] 2. You authenticate users
[x] 3. You implement authorization

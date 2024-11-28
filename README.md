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

[] GET    /api/v1/books              # List all books with pagination
[] GET    /api/v1/books/{id}         # Get book details
[] POST   /api/v1/books              # Add new book
[] PUT    /api/v1/books/{id}         # Update book details
[] DELETE /api/v1/books/{id}         # Delete book
[] GET    /api/v1/books/search       # Search books by title/author/genre


Reading Lists
=============

[] GET    /api/v1/lists              # Get all reading lists
[] GET    /api/v1/lists/{id}         # Get specific reading list
[] POST   /api/v1/lists              # Create new reading list
[] PUT    /api/v1/lists/{id}         # Update reading list
[] DELETE /api/v1/lists/{id}         # Delete reading list
[] POST   /api/v1/lists/{id}/books   # Add book to reading list
[] DELETE /api/v1/lists/{id}/books   # Remove book from reading list


Reviews
=======

[] GET    /api/v1/books/{id}/reviews # Get all reviews for a book
[] POST   /api/v1/books/{id}/reviews # Add new review
[] PUT    /api/v1/reviews/{id}       # Update review
[] DELETE /api/v1/reviews/{id}       # Delete review


Users
======

[] GET    /api/v1/users/{id}         # Get user profile
[] GET    /api/v1/users/{id}/lists   # Get user's reading lists
[] GET    /api/v1/users/{id}/reviews # Get user's reviews



Ensure that:

[] 1. You activate users via email
[] 2. You authenticate users
[] 3. You implement authorization

**Book Recommendation App**
Overview
This project is a simple book recommendation app built using Python in a Jupyter Notebook. It fetches book details and provides recommendations based on either the author or the genre of a queried book. The app utilizes the Open Library API for all data retrieval.

**Features**
-Book Search: Allows users to search for books by title or author. \n
-Recommendations: \n
--By Author: Recommends other books written by the same author. \n
--By Genre: Suggests books in the same genre or category. \n
--Fallback Mechanism: If no similar books by the same author or in the same genre are found, the app recommends a trending book from the Open Library. \n
--Book Details: Displays the title, author, and cover image (if available) for both the queried book and the recommended books.

**How It Works**
-User Input: The user is prompted to enter a book title or author.
-API Request: The app sends a request to the Open Library API to retrieve books matching the query.

**Recommendation Logic:**
-If the user chooses to search by author, the app checks for other books by the same author.
-If the user chooses to search by genre, the app looks for books within the same genre.
-If no similar books are found, the app retrieves a trending book from the Open Library as a fallback.
-Display: The app displays the queried book’s details along with the recommended book(s).

**Dependencies**
-Python 3.x
-requests
-IPython.display for image display in Jupyter Notebook

**Challenges & Solutions**
-Duplicate Recommendations: Initially, the app would recommend different editions of the same book. This was fixed by filtering out duplicate titles and editions.
-API Limitations: The Open Library API sometimes returned unrelated books in recommendations. To address this, a fallback mechanism was implemented to recommend trending books when relevant matches weren’t found.
-Error Handling: Added robust error handling to manage API response issues, ensuring the app continues to function smoothly.

**Conclusion**
This project demonstrates the integration of a public API with Python to create a functional and user-friendly book recommendation system. The implementation of fallback mechanisms ensures that users always receive a recommendation, even when direct matches are unavailable.

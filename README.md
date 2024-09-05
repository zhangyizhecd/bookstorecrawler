# Book Web Crawler Application

## Overview

This project is a **Book Web Crawler** built to extract book information from websites, store the data locally in a JSON file, and provide a UI to interact with the collected data. The application allows users to parse book information, display the parsed results, and manage the book collection through a web interface.

## Features

- **Web Crawling**: Uses `Puppeteer` to scrape book titles, URLs, and image links from a webpage.
- **Data Management**: Allows users to view, add, update, and delete books via a user-friendly UI built with **HTML** and **JavaScript**.
- **Book Display**: Books are displayed in a gallery format, showing the book title, image, and web URL.
- **CRUD Operations**: Full control over book data, including fetching, updating, and deleting information stored in a local JSON file.

## Technical Stack

### Frontend

- **HTML/CSS**: For creating the basic structure and styling of the web pages.
- **JavaScript**: For the client-side logic, including managing DOM elements, making HTTP requests, and handling events.
- **Bootstrap 4**: Used for styling buttons and elements in a responsive manner.

### Backend

- **Node.js & Express**: For setting up the server, handling HTTP requests, and performing CRUD operations on a local JSON file.
- **Puppeteer**: Used for web scraping to extract book data (titles, images, and URLs) from external websites.
- **File System (fs)**: For reading from and writing to JSON files to store book data persistently.

### API Endpoints

- `GET /json_file`: Retrieve book data from a local JSON file.
- `PUT /json_file`: Create or overwrite book data in the JSON file.
- `POST /json_file`: Add new books to the existing JSON file.
- `DELETE /json_file`: Remove the JSON file from the local system.
- `GET /book`: Get details of a specific book by title.
- `PUT /book`: Add a new book to the JSON file.
- `POST /book`: Update an existing book’s details.
- `DELETE /book`: Remove a book from the JSON file.
- `GET /crawler`: Scrape books from a given URL.

## How It Works

1. The user inputs a URL to a book listing page (e.g., Goodreads), and the web crawler scrapes data like the title, image, and book URL using **Puppeteer**.
2. The scraped books are displayed in a gallery format with clickable images and titles that lead to the book's webpage.
3. Users can add, update, or delete books from the collection via the interface.
4. All data is saved in a JSON file on the server, and the UI updates dynamically when books are modified.

## How to Run

1. Install dependencies:
    ```bash
    npm install express puppeteer
    ```
2. Start the backend server:
    ```bash
    node server.js
    ```
3. Open the frontend in a browser by navigating to:
    ```
    http://localhost:8080
    ```

![Crawler Start Page](https://github.com/zhangyizhecd/bookstorecrawler/blob/main/pics/1.png)

**Figure 1: The start page of the bookstore crawler application where users can enter a URL to begin parsing books.**

![Books Display](https://raw.githubusercontent.com/zhangyizhecd/bookstorecrawler/main/pics/2.png)

**Figure 2: After adding the new book, you can view all book imformantion stored**

![Adding New Book](https://raw.githubusercontent.com/zhangyizhecd/bookstorecrawler/main/pics/4.png)

**Figure 3: Form to add a new book manually by providing its title, web URL, and image URL.**

![Updating Book](https://raw.githubusercontent.com/zhangyizhecd/bookstorecrawler/main/pics/5.png)

**Figure 4: Editing an existing book’s details, allowing the user to change the title, web URL, and image URL.**

![Book Deleted](https://raw.githubusercontent.com/zhangyizhecd/bookstorecrawler/main/pics/6.png)

**Figure 5: Confirmation message shown after successfully crawling of book information.**


## Future Enhancements

- **Pagination**: For handling large sets of books.
- **User Authentication**: To allow personalized book collections.
- **Database Integration**: Transition from JSON to a database like MongoDB for better scalability.

## Conclusion

This project demonstrates skills in full-stack development, web scraping, and building RESTful APIs using modern technologies.

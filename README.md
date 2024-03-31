# finalCapstone: Online Bookstore

# Description  

The Final Capstone Project, titled "Online Bookstore," is a web application designed to provide users with a convenient platform for browsing, purchasing, and reviewing books online. With the increasing popularity of e-commerce, especially in the wake of the COVID-19 pandemic, the importance of providing seamless online shopping experiences has become paramount. The Online Bookstore aims to fulfill this need by offering a user-friendly interface, a diverse selection of books, secure payment options, and robust customer support features.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Bookstore</title>
</head>
<body>
    <!-- Your content will go here -->
</body>
</html>


<head>
    <link rel="stylesheet" href="styles.css">
    <!-- Other meta tags -->
</head>


/* styles.css */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}


// data.js
const books = [
    {
        id: 1,
        title: "Book 1",
        author: "Author 1",
        price: 10.99,
        // Add more properties as needed
    },
    // Add more book objects
];


<!-- Inside the <body> tag of index.html -->
<script src="data.js"></script>
<script src="app.js"></script>

// app.js
document.addEventListener("DOMContentLoaded", function() {
    const bookContainer = document.getElementById("book-container");

    // Function to display books
    function displayBooks() {
        books.forEach(book => {
            const bookCard = document.createElement("div");
            bookCard.classList.add("book-card");
            bookCard.innerHTML = `
                <img src="book-image.jpg" alt="${book.title}">
                <h3>${book.title}</h3>
                <p>Author: ${book.author}</p>
                <p>Price: $${book.price}</p>
                <button onclick="addToCart(${book.id})">Add to Cart</button>
            `;
            bookContainer.appendChild(bookCard);
        });
    }

    displayBooks();
});


// Inside app.js
let cart = [];

function addToCart(bookId) {
    const selectedBook = books.find(book => book.id === bookId);
    cart.push(selectedBook);
    // Optionally, you can display a message or update the cart icon
    console.log("Book added to cart:", selectedBook);
}




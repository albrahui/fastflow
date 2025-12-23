# SpareFlow: Intelligent Spare Parts Quotation System

**SpareFlow** is an open-source, lightweight, browser-based application designed to help spare parts retailers and automotive workshops generate professional quotations for their clients with high speed and accuracy. It processes thousands of products locally and generates organized, multi-page PDF documents optimized for A4 printing.

## ✨ Key Features

* **Ultra-Fast Real-Time Search:** Instantly filter products by SKU or Name as you type.
* **Advanced SKU Normalization:** A smart algorithm that ignores spaces, slashes, and hyphens during searches, ensuring you find the right part regardless of how the number is formatted.
* **Smart Pagination:** Automatically distributes products into multiple pages at a rate of **20 items per page**, keeping headers and footers perfectly aligned.
* **Inventory Integration:** The system automatically skips any product where the available `quantity` is 0.
* **Privacy-Focused Output:** Designed to show only essential client details (Name and Phone) while excluding internal data from the final printed version.
* **Zero-Backend Architecture:** Runs entirely in the browser using Vanilla JavaScript—no database or complex server installation required.

## 📂 Data Structure (`data.json`)

The system relies on a `data.json` file to populate the product list. The file must follow this structure to ensure all features function correctly:

```json
{
    "data": [
        {
            "id": 12345,
            "sku": "000 000 00 00",
            "name": "Product name or spare part description",
            "price": 150,
            "quantity": 10,
            "is_available": true
        }
    ]
}
```

# SpareFlow: Intelligent Spare Parts Quotation System

**SpareFlow** is an open-source, lightweight, browser-based application designed to help spare parts retailers and automotive workshops generate professional quotations for their clients with high speed and accuracy. It processes thousands of products locally and generates organized, multi-page PDF documents optimized for A4 printing.

## ✨ Key Features

* **Ultra-Fast Real-Time Search:** Instantly filter products by SKU or Name as you type.
* **Advanced SKU Normalization:** A smart algorithm that ignores spaces, slashes, and hyphens during searches, ensuring you find the right part regardless of how the number is formatted.
* **Smart Pagination:** Automatically distributes products into multiple pages at a rate of **20 items per page**, keeping headers and footers perfectly aligned.
* **Inventory Integration:** The system automatically skips any product where the available `quantity` is 0.
* **Privacy-Focused Output:** Designed to show only essential client details (Name and Phone) while excluding internal data from the final printed version.
* **Zero-Backend Architecture:** Runs entirely in the browser using Vanilla JavaScript—no database or complex server installation required.

## 📂 Data Structure (`data.json`)

The system relies on a `data.json` file to populate the product list. The file must follow this structure to ensure all features function correctly:

```json
{
    "data": [
        {
            "id": 12345,
            "sku": "PART-NUMBER-001",
            "name": "Product name or spare part description",
            "price": 150.00,
            "quantity": 10,
            "is_available": true
        }
    ]
}
```

🛠️ Field Definitions:
sku: The unique part number used for identification and normalization.
name: The description that appears on the client's quotation.
price: The unit price used for automatic total calculations.
quantity: If the value is 0, the part is automatically excluded from search results.

🚀 Getting Started
Download/Clone: Download the files or use git clone to copy the repository.
Add Your Branding: Place your company logo in the root folder named as logo.jpg. Recommended dimensions are 867x247 pixels.
Setup Data: Replace the contents of data.json with your specific product list.
Run Locally: Due to browser security policies (CORS), the file must be run through a simple local server:
Python: python -m http.server 8000
VS Code: Use the "Live Server" extension.
Usage: Navigate to http://localhost:8000 and start generating quotes.

🛠️ Built With
HTML5 & CSS3: Powered by Bootstrap 5 (RTL) for a responsive and clean layout.
JavaScript: Vanilla JS for logic and data management.
PDF Engine: html2pdf.js for high-fidelity HTML-to-PDF conversion.

🤝 Contributing
Contributions are welcome! If you have ideas for improved billing features, VAT support, or external API integrations, feel free to fork the repository and submit a Pull Request.

Note: This project was developed to provide a fast, professional, and free tool for small to medium-sized businesses to organize their quotation workflow.


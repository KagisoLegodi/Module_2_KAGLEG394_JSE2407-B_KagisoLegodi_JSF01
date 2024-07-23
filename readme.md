# Alpine E-store

## Introduction

Welcome to the Alpine E-store! This project is a web application designed to showcase products in a user-friendly manner. It features a detailed view modal to display comprehensive product information, including images, ratings, descriptions, and options to add items to the cart(not yet functional).

## Technologies Used

- **HTML/CSS**: For structuring and styling the components.
- **Alpine.js**: For handling state and interactivity in a lightweight manner.
- **Tailwind CSS**: For utility-first CSS styling.
- **JavaScript**: For additional functionality and dynamic content handling.

## Setup Instructions

To get started with this project, follow these steps:

1. **Clone the Repository**

   git clone <https://github.com/KagisoLegodi/Module_2_KAGLEG394_JSE2407-B_KagisoLegodi_JSF01.git>

2. **Navigate to the Project Directory**

   bash
   cd alpine-final

3. **Install Dependencies**

   Ensure you have Node.js and npm installed, then run:

   bash
   npm install

4. **Run the Development Server**

   Start the development server to view the application locally:

   bash
   npm start

   Open your browser and navigate to `http://localhost:3000` to see the application in action.

## Usage Examples

### Detailed View Modal

The detailed view modal component displays detailed information about a selected product. It features:

- **Product Image**: Displayed on the left side of the modal.
- **Product Title**: Shown prominently at the top.
- **Rating**: Includes a star rating and the number of reviews, if available.
- **Description**: A brief overview of the product.
- **Action Buttons**: Options to add the product to the cart or close the modal.

Here's the HTML structure for the modal:

html

<!-- Detailed View Modal -->
<div x-show="detailViewOpen" class="fixed inset-0 bg-gray-800 bg-opacity-75 flex items-center justify-center z-50">
  <div class="bg-white rounded-lg shadow-md p-4 max-w-3xl mx-auto">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-4">
      <div class="flex justify-center items-center">
        <img :src="selectedProduct.image" alt="Product Image" class="w-2/3 h-auto" />
      </div>
      <div>
        <h1 class="text-2xl font-bold mb-2" x-text="selectedProduct.title"></h1>
        <template x-if="selectedProduct.rating">
          <div class="flex items-center gap-2 mb-2">
            <svg class="w-4 h-4 text-yellow-300" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="currentColor" viewBox="0 0 22 20">
              <path d="M20.924 7.625a1.523 1.523 0 0 0-1.238-1.044l-5.051-.734-2.259-4.577a1.534 1.534 0 0 0-2.752 0L7.365 5.847l-5.051.734A1.535 1.535 0 0 0 1.463 9.2l3.656 3.563-.863 5.031a1.532 1.532 0 0 0 2.226 1.616L11 17.033l4.518 2.375a1.534 1.534 0 0 0 2.226-1.617l-.863-5.03L20.537 8.69a1.534 1.534 0 0 0 .387-1.065z"></path>
            </svg>
            <span x-text="selectedProduct.rating.rate"></span>
            <span x-text="(${selectedProduct.rating.count} reviews)"></span>
          </div>
        </template>
        <p class="text-gray-700 mb-4" x-text="selectedProduct.description"></p>
        <button @click="addToCart(selectedProduct)" class="bg-blue-500 text-white py-2 px-4 rounded">Add to Cart</button>
        <button @click="detailViewOpen = false" class="bg-gray-500 text-white py-2 px-4 rounded mt-2">Close</button>
      </div>
    </div>
  </div>
</div>

## Contributing

We welcome contributions to improve the project. Please follow these guidelines:

1. **Fork the Repository**
2. **Create a Feature Branch**
3. **Commit Your Changes**
4. **Push to the Branch**
5. **Create a Pull Request**

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

# Manorrock E-commerce Free Edition

## Introduction

Manorrock E-commerce Free Edition is an open-source e-commerce platform designed for flexibility and ease of use. This guide will help you install and get started with the Free Edition.

## Prerequisites

- A modern web browser (Chrome, Firefox, Edge, Safari, etc.)
- (Optional) Python 3 or Node.js for testing using a local HTTP server

## Installation Steps


### 1. Download and Extract the Zip Bundle

1. Go to the [releases page](https://github.com/manorrock/manorrock-ecommerce-public/releases) and download the latest zip bundle for the Manorrock E-commerce Free edition.
2. Extract the zip file to your desired location.

### 2. Run the Application Locally

There are two ways to run the Manorrock E-commerce Free Edition locally:

#### Option 1: Open Directly in Your Browser

1. Open the `index.html` file in the exectracted directory with your web browser.
	- Example: `file:///path/to/frontend/free/index.html`
2. Note: Some features (such as loading config.json and products.json) may not work in all browsers due to security restrictions when opening files directly.

#### Option 2: Serve with a Local HTTP Server (Recommended)

1. Open a terminal and navigate to the extracted directory:
	```sh
	cd /your/extracted/directory
	```
2. Start a simple HTTP server:
	- Using Node.js:
	  ```sh
	  npx serve .
	  ```
	- Or using Python 3:
	  ```sh
	  python3 -m http.server
	  ```
3. Open your browser and go to `http://localhost:8000/` (or the port shown in your terminal).

### 3. Customizing the installation

You can easily customize your store using the following files in your extracted directory:

- `config.json`: Store configuration (titles, welcome message, order email, etc.)
- `products.json`: List of products to display in your store

### Example: config.json

```json
{
	"orderEmail": "orders@store.example.com",
	"welcomeTitle": "Welcome to your free E-commerce store",
	"welcomeContent": "You should read our instructions for light customization",
	"navbarTitle": "Manorrock E-Commerce Free",
	"routerType": "hash"
}
```

### Example: products.json

```json
[
	{
		"id": 1,
		"name": "Sample Product 1",
		"price": 10.0,
		"description": "A great product.",
		"image": "https://via.placeholder.com/150"
	},
	{
		"id": 2,
		"name": "Sample Product 2",
		"price": 20.0,
		"description": "Another great product.",
		"image": "https://via.placeholder.com/150"
	},
	{
		"id": 3,
		"name": "Sample Product 3",
		"price": 30.0,
		"description": "Yet another great product.",
		"image": "https://via.placeholder.com/150"
	}
]
```

Edit these files to update your store's branding and product catalog. Changes are reflected immediately when you reload the page (running locally).

### 4. Deploying to GitHub Pages

You can easily host your Manorrock E-commerce Free Edition site on GitHub Pages:

1. Create a new GitHub repository (or use an existing one).
2. Copy all the files from your extracted Free Edition bundle into the repository (typically in the root or a `docs/` folder).
3. Commit and push the files to your repository.
4. In your repository settings, enable GitHub Pages and set the source to the branch and folder where your files are located (e.g., `main` branch and `/` root or `/docs`).
5. After a few minutes, your site will be available at `https://<your-username>.github.io/<your-repo>/`.

**Note:**
- If your site is not at the root (e.g., `/docs`), make sure your `config.json` and `products.json` paths are correct and use hash-based routing (`"routerType": "hash"` in `config.json`).
- For more details, see the [GitHub Pages documentation](https://docs.github.com/en/pages).

## Free to use

While Manorrock E-commerce Free Edition is not open source it is free to use.

## Disclaimer of Liability

This software is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors or copyright holders be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the software or the use or other dealings in the software.

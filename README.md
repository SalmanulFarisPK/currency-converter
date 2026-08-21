# currency-converter
A simple and responsive currency converter built with HTML, CSS, and JavaScript, using live exchange-rate data from an external API.


# 💱 Currency Converter

A simple and responsive **Currency Converter web application** built using **HTML, CSS, and JavaScript**. The application allows users to select two currencies, enter an amount, and convert it using live exchange-rate data from an external currency API.

## ✨ Features

- 🌍 Supports multiple currencies
- 💱 Select **From** and **To** currencies
- 💵 Enter a custom amount to convert
- 🚩 Automatically updates the country flag when a currency is selected
- 🔄 Fetches exchange-rate data from an external API
- ⚡ Calculates the converted amount instantly
- 🎨 Simple and clean user interface
- 📱 Uses a basic responsive viewport configuration

## 🛠️ Technologies Used

- **HTML5** – Structure of the application
- **CSS3** – Styling and layout
- **JavaScript (ES6)** – Application logic and API integration
- **Font Awesome** – Swap/conversion icon
- **FlagsAPI** – Country flag images
- **Currency API** – Exchange-rate data

## 📁 Project Structure

```text
currency-converter/
│
├── index.html
├── style.css
├── script.js
├── countryList.js
└── README.md
```

## 🔌 APIs Used

### Currency API

The application retrieves exchange-rate data from:

```text
https://latest.currency-api.pages.dev/v1/currencies/
```

For example, when USD is selected as the source currency, the application requests:

```text
https://latest.currency-api.pages.dev/v1/currencies/usd.json
```

The application then reads the exchange rate for the selected target currency.

### Flags API

Country flags are loaded from:

```text
https://flagsapi.com/
```

The selected currency is mapped to a country code in `countryList.js`, which is then used to display the corresponding flag.

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

### 2. Open the project

Navigate into the project directory:

```bash
cd YOUR-REPOSITORY
```

### 3. Run the project

You can simply open `index.html` in a browser.

For development, it is recommended to use **VS Code with the Live Server extension**.

## 🧩 How It Works

1. The currency list is loaded from `countryList.js`.
2. JavaScript dynamically creates the currency options in the two dropdowns.
3. When a currency changes, `updateFlag()` updates the corresponding country flag.
4. When the **Convert** button is clicked:
   - The entered amount is read.
   - The selected source and target currencies are obtained.
   - The source currency API endpoint is requested.
   - The exchange rate is extracted from the API response.
   - The amount is multiplied by the exchange rate.
   - The converted value is displayed on the page.

### Conversion Formula

```text
Converted Amount = Amount × Exchange Rate
```

For example:

```text
100 USD × USD/INR exchange rate = INR equivalent
```

## 📄 Main Files

### `index.html`

Contains the main user interface, including:

- Amount input
- From-currency dropdown
- To-currency dropdown
- Country flags
- Conversion result
- Convert button

### `style.css`

Contains the visual design of the application, including:

- Page layout
- Currency converter card
- Dropdown styling
- Input styling
- Button styling
- Colors and spacing

### `script.js`

Contains the application logic, including:

- Currency dropdown generation
- Flag updates
- API requests
- Exchange-rate extraction
- Currency conversion
- Result display

### `countryList.js`

Contains the currency-code-to-country-code mapping used by the application to display the correct flags.

## ⚠️ Notes

- Exchange rates are provided by the external Currency API and may change over time.
- The application requires an internet connection to retrieve exchange-rate data and flag images.
- API availability can affect the conversion functionality.
- This project is intended as a learning project for practicing JavaScript, DOM manipulation, and API integration.

## 📸 Preview

The application provides a simple interface where users can enter an amount, choose the source and destination currencies, and view the converted value.

⭐ If you found this project useful, consider giving the repository a star!

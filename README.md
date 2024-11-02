# Bankist App

A minimalistic banking application that enables users to track transactions, check account balances, transfer funds, request loans, and manage accounts. This web-based application simulates basic bank functionalities, enhancing user experience with formatted date, time, and currency displays based on different locales. [TRY NOW](https://qyuzet.github.io/js-bankist-app/)

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Data Structure](#data-structure)
- [Event Handlers](#event-handlers)
- [License](#license)

## Features

- **User Login**: Authentication with a PIN for each user.
- **Transaction History**: Display of past transactions with formatted date and type (deposit/withdrawal).
- **Balance and Summary**: Overview of the current balance and a breakdown of income, outgoing, and interest.
- **Fund Transfers**: Transfer funds to other users within the app.
- **Loan Requests**: Request loans if certain criteria are met.
- **Account Closure**: Delete account upon entering valid credentials.
- **Logout Timer**: Automatic logout after a period of inactivity.
- **Currency and Locale Formatting**: Localized currency display based on user’s region and account currency.

## Technologies Used

- **JavaScript (ES6)**: Core application functionality.
- **HTML5/CSS3**: Basic front-end structure and styling.
- **Intl API**: For formatting dates, times, and currency.

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/bankist-app.git
   cd bankist-app
   ```

2. Open `index.html` in a browser to run the app.

## Usage

1. **Login**: Use predefined usernames and PINs to access accounts:
   - Example:
     - Username: `rs` (for `Riki Syahputra`)
     - PIN: `1111`
   
2. **Viewing Transactions**: Once logged in, transactions will appear in chronological order.

3. **Transferring Funds**: Specify recipient username and amount to transfer. (Only transfers to other users are allowed).

4. **Requesting a Loan**: Loans are approved if any deposit is at least 10% of the requested amount.

5. **Closing Account**: Enter username and PIN in the ‘Close Account’ section.

6. **Sorting Transactions**: Use the sort button to toggle between chronological and ascending transaction views.

## Data Structure

- `accounts`: An array containing account objects with information such as:
  - `owner`: Account holder’s name.
  - `movements`: Array of transaction amounts (positive for deposits, negative for withdrawals).
  - `movementsDates`: Array of dates corresponding to each transaction.
  - `currency` and `locale`: Format settings for each account.

### Example Account Data

```javascript
const account1 = {
  owner: 'Riki Syahputra',
  movements: [200, 455.23, -306.5, 25000, -642.21, -133.9, 79.97, 1300],
  interestRate: 1.2,
  pin: 1111,
  movementsDates: ['2019-11-18T21:31:17.178Z', ...],
  currency: 'EUR',
  locale: 'pt-PT',
};
```

## Event Handlers

- **Login (`btnLogin`)**: Authenticates and loads account data.
- **Transfer (`btnTransfer`)**: Validates and processes fund transfers between users.
- **Loan Request (`btnLoan`)**: Verifies and processes loan requests.
- **Account Closure (`btnClose`)**: Deletes the account if credentials are correct.
- **Sort Transactions (`btnSort`)**: Sorts transactions by amount.

## License

This project is licensed under the MIT License.

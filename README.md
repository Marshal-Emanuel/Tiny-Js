# Tiny-Js is lightweight consumption of Tinypesa in Javascript
STK Push Library

Introduction

This library (name to be confirmed) provides a convenient way to integrate Mobile Money STK Push (Sim Toolkit Push) functionality into your JavaScript applications. With STK Push, you can initiate mobile payment transactions directly from a user's mobile phone, offering a seamless and secure payment experience.

Prerequisites

A supported mobile money provider with STK Push capabilities (e.g., M-Pesa, Airtel Money, etc.)
A merchant account with your mobile money provider
A basic understanding of JavaScript and HTTP requests
Installation

The specific installation method will depend on the library's distribution model. Here are some common possibilities:

npm Package:
If the library is available as an npm package, you can install it using the following command:

Bash
npm install stk-push-library
Use code with caution.
Standalone Script:
If the library is provided as a standalone JavaScript file, you'll need to download it and include it in your HTML file using a <script> tag:

HTML
<script src="stk-push-library.js"></script>
Use code with caution.
Usage

Import or Include the Library:

If using npm, import the library in your JavaScript code:

JavaScript
const stkPush = require('stk-push-library');
Use code with caution.
If using a standalone script, the library functions should be available globally within your JavaScript code.

Initiate an STK Push Transaction:

Call the appropriate library function to initiate an STK Push transaction. The exact function name and parameters might vary depending on the library's implementation, but typically it will involve providing details like:
Phone Number: The recipient's mobile phone number.
Amount: The amount to be transferred.
Currency: The currency of the transaction (e.g., KES, USD).
Description (Optional): A brief description of the transaction.
Callback URL (Optional): A URL on your server to receive a notification upon transaction completion (success or failure).
Here's a general example (replace placeholders with actual values):

JavaScript
stkPush.initiateTransaction({
  phoneNumber: '+254712345678',
  amount: 100,
  currency: 'KES',
  description: 'Payment for Order #12345',
  callbackUrl: 'https://your-server.com/stk-push-callback'
})
.then(response => {
  console.log('STK Push initiated successfully:', response);
})
.catch(error => {
  console.error('Error initiating STK Push:', error);
});
Use code with caution.
Handle the Transaction Response (Optional):

If you provided a callback URL, your server will receive a notification from the mobile money provider upon transaction completion. You'll need to implement logic on your server to handle this notification and update your application's state accordingly (e.g., display a success or failure message to the user).
Important Considerations

Refer to the specific documentation of the chosen STK Push library for detailed instructions and code examples.
Ensure you have the necessary permissions and configurations set up with your mobile money provider for STK Push functionality.
Implement proper error handling and security measures in your application to handle potential issues during the STK Push process.

# FundamentalsCertificateApp


**I. Overview**

The project was created using the empty-skeleton template, with the objective of allowing a customer to make purchases at a computer store and have a courier take those purchases to the customer's home. The customer has to have a bank account and a computer store account in order to do the shopping.

**II. Workflow**
1.	The customer and the computer store must have a bank account;
2.	The customer must have an account at the computer store.
3.	When the customer has an account at the computer store, he can order a list of products that he wants to buy;
4.	The computer store accepts or rejects the order with the products and number of products chosen by the customer;
5.	After the computer store accepts the order it will immediately call a courier;
6.	The courier must always accept to take the purchases to the customer's home;
7.	The customer can accept or reject the purchases;
8.	8.	After the customer accepts, a transaction is made from the customer's bank account to the computer store's bank account;
9.	Finally, an invoice is created with the customer's purchase.

**III. Parties**

- Store – Computer store;
- Client – Person who buys the products in the computer store;
- Courier – Person who takes the products to the customer's home;
- Bank – Bank where the customer has money to pay for purchases at the computer store;
- Other – Other parties used to unhappy test.

**IV. Choices**

| Template | Choice | Description |
| -------------------------- | -------------------------------- | ---------------- |
| Bank | CreateAccountBankProposal | This choice serves to client propose create account in the bank |
| BankAccountProposal | RejectBankAccountProposal | This choice serves to bank reject create account in the bank |
| BankAccountProposal | CreateAccountBank | This choice serves to bank approve and create account in the bank |
| BankAccount | CreditAmount | This choice serves to bank accept the credit amount to the customer's |
| BankAccount | DebitAmount | This choice serves to bank accept the debit the customer's account |
| Store | CreateAccountStoreProposal | This choice creates a new proposal to create an account in the store |
| Store | AddStockProducts | This choice serves to add new products to the stock |
| ClientAccountStoreProposal | RejectStoreAccountProposal | This choice allows reject the proposal to create an account |
| ClientAccountStoreProposal | CreateAccountStore | This choice serves to create account store |
| ClientAccountStore | - | - |
| StockProducts | AddProductToStock | This choice add products to stock |
| StockProducts | OrderProductProposal | This choice create a proposal to product orders |
| StockProducts | UpdateProductToStock | This choice update the product stock or not if the number of produtos is equals 0 or less |
| OrderProduct | ValidateOrderByStore | This choice validate the order by the store and accept or reject the order |
| OrderCourier | ApproveOrderByClient | This choice approve the purchase by the customer |
| OrderCourier | RejectOrderByClient | This choice reject the order by the customer |
| TransactionPaymentDebit | ValidateTransactionPaymentDebit | This choice validates the debit amount transaction |
| TransactionPaymentCredit | ValidateTransactionPaymentCredit | This choice credits the amount to a new account |
| Transaction | - | - |


**V. Diagram**

-----------

**VI. Tests**

-----

**VII. Notes**

 - This project was created with Daml version 2.6.0.

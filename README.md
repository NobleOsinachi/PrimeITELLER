# PRIMEBanking API

This repository contains the source code for a banking API that facilitates various banking operations. The API is designed to handle single transactions, transaction reversals, batch postings, account inquiries, name inquiries, balance inquiries, and BVN (Bank Verification Number) inquiries.

**Project Structure**

The banking API is built using C# and ASP.NET framework. It is organized into three main controllers:

1. **BankingOperationController**: This controller handles single transactions and transaction reversals. It exposes two POST endpoints:
   - `/Prime/SingleTransaction`: Accepts a JSON payload containing transaction details and processes the single transaction.
   - `/Prime/ReversalFTPostTrans`: Accepts a JSON payload for a transaction and initiates a reversal for the specified transaction.

2. **CustomerServiceController**: This controller is responsible for customer-related operations like bulk account inquiries, account inquiries, name inquiries, balance inquiries, BVN inquiries, and transaction status inquiries. It exposes several endpoints, each handling a specific operation.

3. **AuthenticationController**: This controller handles user authentication-related tasks. It provides endpoints to validate user credentials and retrieve user details.

**Database Connection**

The API uses a SQL Server database to store and retrieve data related to banking operations and customer details. The connection to the database is established using Entity Framework.

**Logging**

The API incorporates NLog to log various events and activities during the processing of requests. The logs are essential for monitoring and debugging purposes.

**Usage**

To use the banking API, you can deploy it on a web server that supports ASP.NET applications. Ensure that the necessary database connectivity and configuration settings are properly set before deploying the API. The API can be consumed by making HTTP requests to its various endpoints.

**Endpoints**

Below are the main endpoints provided by the banking API:

1. `/Prime/SingleTransaction`: Initiates a single transaction and returns the transaction status.

2. `/Prime/ReversalFTPostTrans`: Initiates a transaction reversal based on the provided details.

3. `/Prime/BatchPosting`: Performs batch posting of multiple transactions simultaneously.

4. `/Prime/AccountEnquiry`: Retrieves account details based on the provided account number.

5. `/Prime/NameEnquiry`: Performs a name enquiry based on the provided account number and country code.

6. `/Prime/BalanceEnquiry`: Performs a balance enquiry based on the provided account number and country code.

7. `/Prime/BvnEnquiry`: Retrieves BVN details based on the provided account number and bank code.

8. `/Prime/GetTransactionStatus`: Retrieves the status of a transaction based on the provided request ID, country code, and client reference ID.

9. `/Prime/ValidateUser`: Validates user credentials for authentication.

10. `/Prime/GetUserDetails`: Retrieves user details based on the provided user credentials.

**Disclaimer**

This banking API is provided as-is and may require further customization and integration to suit specific banking systems. It is essential to ensure proper security measures are implemented to protect sensitive data and prevent unauthorized access.

**Contributing**

If you find any issues or have suggestions for improvements, feel free to create an issue or submit a pull request. Contributions to enhance the functionality and reliability of the API are welcome.

**License**

This banking API is released under the [MIT License](https://opensource.org/licenses/MIT). Please review the license file for detailed terms and conditions.

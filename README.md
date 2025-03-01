# CheckIfConnectedToInternet: Delphi Internet Connectivity Checker

## Overview
The `CheckIfConnectedToInternet` Delphi program allows users to check if their machine is connected to the internet. It uses the `IdHTTP` component to send a request to a remote server (in this case, Google) and checks for a response to determine the internet connection status.

## Features
- **Internet Connectivity Check**: Verifies if the system is connected to the internet by making an HTTP request.
- **User Feedback**: Displays the current status of the internet connection in a label.
- **Simple Interface**: Includes a button that the user clicks to check connectivity.

## How It Works
The program uses the `TIdHTTP` component to attempt a GET request to `http://www.google.com`. If the connection is successful, the program updates a label indicating that the system is connected to the internet. If the request fails, it shows that the system is not connected.

### Code Explanation
- **IsInternetConnection**: This function attempts to make an HTTP request to `http://www.google.com`. If successful, it returns `True`, indicating the machine is connected to the internet. If the request fails (e.g., no internet connection), it returns `False`.
- **btnInternetClick**: This event handler is triggered when the user clicks the "Check Connection" button. It calls `IsInternetConnection` and updates the label with the connection status.

## Usage
1. Run the Delphi application.
2. Click the **Check Connection** button to test if the system is connected to the internet.
3. The label will display:
   - `Status: Connected To The Internet` if the connection is successful.
   - `Status: NOT Connected To The Internet` if the connection fails.

## Technologies Used
- **Delphi (VCL framework)**
- **IdHTTP (Indy library)**
- **Internet Connectivity Check via HTTP Requests**

## Potential Enhancements
- **Timeout Control**: Allow the user to customize the timeout duration for the internet check.
- **Custom Server URL**: Enable users to specify their own server URL for the connectivity check.
- **Retry Mechanism**: Automatically retry the check a few times before showing the result.

## Author
**Veer Gosai**  
This program was created to demonstrate how to check for internet connectivity in Delphi using the `IdHTTP` component.

---
This document serves as a guide for understanding and improving the CheckIfConnectedToInternet Delphi program.

# API Endpoints Documentation

## Overview
This document provides details about the API endpoints available in the Crecemax WhatsApp Bot.

## Endpoints

### 1. Send Message
- **Endpoint:** `/send-message`
- **Method:** POST
- **Description:** This endpoint allows users to send messages via WhatsApp.
- **Request Body:**
  - `phoneNumber`: String, the phone number of the recipient.
  - `message`: String, the message content to be sent.

### 2. Receive Message
- **Endpoint:** `/receive-message`
- **Method:** POST
- **Description:** This endpoint receives messages sent to the bot.
- **Request Body:**
  - `sender`: String, the phone number of the sender.
  - `message`: String, the content of the received message.

### 3. Get User Info
- **Endpoint:** `/user-info`
- **Method:** GET
- **Description:** This endpoint retrieves user information.
- **Query Parameters:**
  - `userId`: String, the ID of the user for whom to fetch information.

### 4. Get Bot Status
- **Endpoint:** `/bot-status`
- **Method:** GET
- **Description:** This endpoint checks the current status of the bot.

## Authentication
- All endpoints require an API key for authentication. Include the API key in the request headers as follows:
  - `Authorization: Bearer YOUR_API_KEY`

## Error Handling
- Errors are returned in a standard format:
  - `status`: Integer, the HTTP status code.
  - `message`: String, a detailed error message.
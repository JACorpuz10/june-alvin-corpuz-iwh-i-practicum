# Integrating With HubSpot I: Foundations Practicum

## Project Overview

This project was developed as part of the **Integrating With HubSpot I: Foundations** certification practicum from HubSpot Academy.

The application demonstrates how to integrate a Node.js application with HubSpot CRM using REST APIs.

The project uses the standard **Contacts** object as an alternative to a custom object, as permitted by the practicum instructions when custom-object access is unavailable.

## Technologies Used

- Node.js — JavaScript runtime environment
- Express.js — Web application framework
- Axios — HTTP requests to the HubSpot CRM API
- Pug — HTML templating engine
- CSS — Application styling
- dotenv — Environment variable management
- Git and GitHub — Version control

## Application Features

**1. Display HubSpot Contacts**

The homepage retrieves contact records from HubSpot using an HTTP GET request and displays them in an HTML table.

**2. Create New Contacts**

The application provides an HTML form that allows users to create new HubSpot contacts using an HTTP POST request.

**3. Automatic Redirect**

After successfully creating a contact, the application redirects the user to the homepage, where the updated contact list is displayed.

## HubSpot CRM Properties

The application uses three standard contact properties:

| Property | Internal Name |
|---|---|
| First Name | `firstname` |
| Last Name | `lastname` |
| Email | `email` |

Three custom contact properties were also created:

| Property | Internal Name | Field Type |
|---|---|---|
| Name | `test_name` | Single-line text |
| Category | `test_category` | Single-line text |
| Status | `test_status` | Single-line text |

## Application Routes

| Method | Route | Description |
|---|---|---|
| GET | `/` | Retrieve and display HubSpot Contacts |
| GET | `/update-cobj` | Render the new contact form |
| POST | `/update-cobj` | Create a new HubSpot Contact and redirect to the homepage |


## HubSpot Developer Test Account

This practicum uses the standard Contacts object
as permitted by the practicum instructions.

**HubSpot Account ID:** 247734644

**CRM Object:** Contacts (Standard Object)

**Contacts List View:**

[View HubSpot Contacts](https://app-na2.hubspot.com/contacts/247734644/objects/0-1/views/all/list)


## Installation and Setup

**Step 1: Clone the repository**

Clone this forked GitHub repository to your local development environment.

**Step 2: Install dependencies**

Run `npm install`.

**Step 3: Configure environment variables**

Create a `.env` file in the project root containing:

`HUBSPOT_PRIVATE_APP_TOKEN=your_private_app_token`

The token must come from the HubSpot developer test account and have the required Contacts read and write permissions.

**Step 4: Start the application**

Run `node index.js`.

**Step 5: Open the application**

Homepage: `http://localhost:3000`

Create Contact Form: `http://localhost:3000/update-cobj`

## Security

The application uses environment variables to protect HubSpot API credentials.

The `.env` file and private app access token must never be committed or uploaded to GitHub.

## Practicum Requirements Demonstrated

- Integration with the HubSpot CRM API
- HTTP GET and POST requests
- Three Express routes
- Two Pug templates (`homepage.pug` and `updates.pug`)
- Contact record creation and retrieval
- Standard and custom CRM properties
- Git version control and repository management

## Certification

**Course:** Integrating With HubSpot I: Foundations

**Practicum:** Node.js and HubSpot CRM API Integration

**Author:** June Alvin Corpuz

[HubSpot Academy Practicum Instructions](https://app.hubspot.com/academy/l/tracks/1092124/1093824/5493?language=en)

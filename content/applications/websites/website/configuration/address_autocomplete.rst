====================
Address Autocomplete
====================

To ensure that your customers' delivery addresses exist and are understood by the carrier,
you can use Google Places API on your website.
To do so, go to :guilabel:`Settings → SEO → enable “Address Autocomplete”`.


.. image:: address_autocomplete/enable-address-autocomplete.png
   :alt: Enable address autocomplete

.. warning::
   You need to generate your own API key, this one is only an example.

But first, you need to generate a :guilabel:`Google Places API key`. This involves a few steps.
The Places API allows developers to access detailed information about places using HTTP requests.
Here's a short documentation guide on how to create your ID for the Google Places API:

Step 1: Enable the Places API
-----------------------------

Go to the `Google Cloud Console <https://console.cloud.google.com/getting-started>`_:

**Create a New Project:**
If you don't have a project, create one by clicking on the project dropdown in the top right corner and selecting
"New Project."
Follow the prompts to set up your project.

**Enable the Places API:**
In the Cloud Console, go to the `APIs & Services > Dashboard <https://console.cloud.google.com/apis/dashboard>`_
and click on "+ ENABLE APIS AND SERVICES."
Search for :guilabel:`"Places API"` and select it. Click on the :guilabel:`"Enable"` button.

Step 2: Create API Credentials
------------------------------

In the Cloud Console, go to `APIs & Services > Credentials <https://console.cloud.google.com/apis/credentials>`_.

**Create Credentials:**
Click on the :guilabel:`"Create Credentials"` button and select :guilabel:`"API key."`
A pop-up appears with your API key.

**Restrict the API Key (Optional):**

.. note::
   For security purposes, you can restrict `the usage of your API key.
   Under the :guilabel:`"API restrictions"` section, you can specify which APIs your key can access.
   For the Places API, you can restrict it to only allow requests from specific websites or apps.

.. important::
   Save Your API Key: Copy your API key and securely store it.
   Do not share it publicly or expose it in client-side code.

Step 3: Usage
-------------

Now that you have your API key, you can start using it in your applications to make requests to the Google Places API.
Include the API key in your requests using the key parameter.

.. important::
   Remember to check the `Google Places API documentation <https://console.cloud.google.com/apis/credentials>`_
   for details on the available endpoints, request parameters, and response formats.
   Ensure compliance with Google's usage policies and guidelines when using the Places API in your applications.

   **API Key Security:**
   Always keep your API key secure and do not expose it in publicly accessible code or repositories.
   Use API key restrictions to control which APIs and services your key can access.

   **Pricing and Quotas:**
   Understand the pricing model of the Google Places API and be aware of usage quotas and limits.
   Regularly monitor your API usage and set up billing to ensure uninterrupted service.

   **Terms of Service:**
   Familiarize yourself with Google's Maps Platform Terms of Service and adhere to them.
   Ensure compliance with usage policies, such as not using the API for illegal or abusive purposes.

   **Billing and Payment:**
   Set up billing for your Google Cloud Platform project to avoid service interruptions.
   Review the pricing details to estimate costs associated with your usage.

   **API Documentation:**
   Thoroughly read the Google Places API documentation to understand the available endpoints, parameters,
   and response formats.
   Stay updated on any changes or updates to the API by regularly checking the documentation.

   **Request and Response Formats:**
   Be aware of the request and response formats required by the API, including the correct structure of API requests
   and the interpretation of responses.

   **Rate Limiting:**
   Understand the rate limiting applied by the Google Places API to avoid exceeding usage limits.
   Implement error handling and retry mechanisms in your code to handle rate-limited scenarios.

   **Geocoding vs. Places API:**
   Distinguish between the Google Places API and the Geocoding API. The Places API is focused on retrieving information
   about places, while the Geocoding API is used for converting addresses into geographic coordinates.

   **User Experience Considerations:**
   Provide a clear user interface attribution in your application if required by the terms of service.
   Ensure a positive user experience by presenting place information in a meaningful and accessible way.

   **Legal and Compliance:**
   Respect the legal rights and privacy of users when implementing location-based services.
   Be aware of data protection laws and regulations that may apply to the use of location data.

   **Support and Community:**
   Utilize the Google Cloud Community and Google Maps Platform Support for assistance and information.
   By following these guidelines and staying informed about updates and best practices, you can create a reliable and
   compliant integration with the Google Places API.

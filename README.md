# Overview
Postman collection for Vonage Meeting API REST API with basic parameters and request body sample. The collection includes pre-request script which automatically generates JSON web token based on your Vonage credentials.  
<img width="222" alt="Screenshot 2023-05-19 at 10 51 48" src="https://github.com/ydumburs/vonage-video-api-postman-collection/assets/45432538/55b28857-9b24-4bad-9c8a-2216ffe90ed6">

# Applies To
- [Vonage Meeting REST API](https://developer.vonage.com/api/meetings)
- [Vonage Reports API](https://developer.vonage.com/en/api/reports)

# Prerequisites
This requires a Vonage account. If you don’t have one already, you can [sign up](https://ui.idp.vonage.com/ui/auth/registration). 

# Set up
1. Download [Postman](https://www.postman.com/downloads/) desktop app if you haven't installed it yet. You can also use [the Web version](https://blog.postman.com/announcing-postman-for-the-web-now-in-open-beta/).
2. Import the Environment template `Vonage Meeting API.postman_environment.json`. (Ref. [Adding environment variables](https://learning.postman.com/docs/sending-requests/managing-environments/#adding-environment-variables))
3. Add your credentials to the imported Environment. Make sure you add them on `CURRENT VALUE`.  
The minimum required to generate a JWT is `jti`, `application_id`, and `private_key`. If you use Reports API please input your Vonage API Key and Secret into `vonage_api_key` and `vonage_api_secret`. You can add other values such as `callback_url` as appropriate.
- `jti` = Set jti to a unique identifier for the JWT token. (Ref. [JSON web token spec](https://datatracker.ietf.org/doc/html/rfc7519#section-4.1.7)) 
- `application_id` = Your application ID (You need to create an application from https://dashboard.nexmo.com/applications with `Meeting API` capability enabled.)
- `private_key` = Your application private key (Open the application page from https://dashboard.nexmo.com/applications and click `Edit` -> `Generate public and private key` then private key file will be downloaded.)  
- `vonage_api_key` = Your Vonage account API key (You can find it from https://dashboard.nexmo.com/.) 
- `vonage_api_secret` = Your Vonage account secret (You can find it from https://dashboard.nexmo.com/.) 
4. Import the collection `Vonage Meeting API.postman_collection_x.json` into Postman. (Ref. [Importing Postman data](https://learning.postman.com/docs/getting-started/importing-and-exporting-data/#importing-postman-data))

# How to make REST requests
1. Make sure the correct Environment is selected.
2. Select a request from the imported Collection and click on the `Send` icon.
3. Find a response.

# Reference
- The script refers an external library http://kjur.github.io/jsrsasign/jsrsasign-latest-all-min.js.  

# Disclaimer
This is provided AS IS and not supported by Vonage team. Use it at your own risk.

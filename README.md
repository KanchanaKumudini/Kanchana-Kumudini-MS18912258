# Kanchana-Kumudini-MS18912258
https://github.com/KanchanaKumudini/Kanchana-Kumudini-MS18912258/network/members

Step 1 - Register your App in Facebook Developer Website

1.1 Create an application in the developer account on Facebook by using https://developers.facebook.com/ and add your new application.

![image](https://user-images.githubusercontent.com/50174329/58014475-8907d680-7b16-11e9-8f62-c771821cd6c3.png)

1.2 Type the display name of your application and your contact email to create the application.

![image](https://user-images.githubusercontent.com/50174329/58014955-ab4e2400-7b17-11e9-9c8a-7706f9f8d3d2.png)

1.3 Associate “Facebook Login” with your application.

![image](https://user-images.githubusercontent.com/50174329/58015317-87d7a900-7b18-11e9-93eb-6ad191a265da.png)

1.4 Provide the Redirection Endpoint URL under the Settings of the “Facebok Login”.

![image](https://user-images.githubusercontent.com/50174329/58015700-8a86ce00-7b19-11e9-9230-bd115c8b8b91.png)

1.5 Obtain your App ID, App Secret and the Redirection Endpoint URL.

![image](https://user-images.githubusercontent.com/50174329/58015872-f5380980-7b19-11e9-938e-fd461fe46edf.png)

App ID = 447467986082418
App Secret = 363a41d88276ec4fd709ff51e2feca13
Redirection Endpoint URL = http://localhost:8080/facebookapp/callback

Step 2 - Obtaining the Authorization Code

2.1 Send a HTTP GET request to the Authorize Endpoint of Facebook to obtain the authorization code from facebook using https://www.facebook.com/dialog/oauth.

![image](https://user-images.githubusercontent.com/50174329/58016538-7c39b180-7b1b-11e9-94ee-0b89960f82d2.png)

2.2 Prepare the following URL using the above values.

https://www.facebook.com/dialog/oauth?response_type=code&client_id=447467986082418&redirect_uri=http%3A%2F%2Flocalhost%3A8080%2Ffacebookapp%2Fcallback&scope=public_profile%20user_posts%20user_friends%20user_photos

2.3 View the User Contect Page.

![image](https://user-images.githubusercontent.com/50174329/58016921-9b850e80-7b1c-11e9-8250-7a9023a1abe5.png)

2.4 Press Continue and facebook will redirect the browser to the Redirection Endpoint URL.




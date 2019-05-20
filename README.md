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

![image](https://user-images.githubusercontent.com/50174329/58017302-7b098400-7b1d-11e9-832c-1e3213f9a510.png)

2.5 Get the URL from the browser.

http://localhost:8080/facebookapp/callback?code=AQCPK2oPP0jNwNdWixP29lr9DzPTpVaFhJxa4I61VGUIx6mq5z9WpO_tXL5qTx6E2vkj1w53_hOUZrdghCOieK7ysQfD59NzfLTcO8Bxs_vhzMV73uAwls2SqR2IpN1Yzcu1BeS2bdI4zUqoDLt-utUmKrmXD-iw58XpYDrr06_acl7kVo112UdgsTWNrYBNXsYDx1GVCI53B45nqoEJYgtMdsngQV_1swNjvx2cdCIztyt5DvqFBk6ntVCY26Ag3FiYD0QipBTQOxfW1StSXO-tC_USWnAvG2mwV5rBHuqRCDuQiX_Ke6vuq-lzTjqVpe4#_=_

Authorization code value = AQCPK2oPP0jNwNdWixP29lr9DzPTpVaFhJxa4I61VGUIx6mq5z9WpO_tXL5qTx6E2vkj1w53_hOUZrdghCOieK7ysQfD59NzfLTcO8Bxs_vhzMV73uAwls2SqR2IpN1Yzcu1BeS2bdI4zUqoDLt-utUmKrmXD-iw58XpYDrr06_acl7kVo112UdgsTWNrYBNXsYDx1GVCI53B45nqoEJYgtMdsngQV_1swNjvx2cdCIztyt5DvqFBk6ntVCY26Ag3FiYD0QipBTQOxfW1StSXO-tC_USWnAvG2mwV5rBHuqRCDuQiX_Ke6vuq-lzTjqVpe4#_=_

Step 3 - Obtaining the Access Token

3.1 Send a HTTP POST request to the Token Endpoint https://graph.facebook.com/oauth/access_token of facebook with the authorization code received in the previous step. 

![image](https://user-images.githubusercontent.com/50174329/58018176-bc9b2e80-7b1f-11e9-9e3c-d95988cf2a19.png)

3.2 Prepare the authorization header with the App credentials.

App ID = 447467986082418
App Secret = 363a41d88276ec4fd709ff51e2feca13
AppID:AppSecret = 447467986082418:363a41d88276ec4fd709ff51e2feca13
Base64(AppID:AppSecret) = NDQ3NDY3OTg2MDgyNDE4OjM2M2E0MWQ4ODI3NmVjNGZkNzA5ZmY1MWUyZmVjYTEz

3.3 Add the header as follows:

Authorization: Basic NDQ3NDY3OTg2MDgyNDE4OjM2M2E0MWQ4ODI3NmVjNGZkNzA5ZmY1MWUyZmVjYTEz

3.4 Use a HTTP Client browser plugin like RESTClient send the request.

![image](https://user-images.githubusercontent.com/50174329/58018900-bf971e80-7b21-11e9-95e7-5f10630c6292.png)

![image](https://user-images.githubusercontent.com/50174329/58034261-c9ca1480-7b43-11e9-9e42-cb928bcc3c77.png)

![image](https://user-images.githubusercontent.com/50174329/58033919-06e1d700-7b43-11e9-8af4-4ef1bb620bad.png)

3.5 Obtain the Access Token.

![image](https://user-images.githubusercontent.com/50174329/58019023-1b61a780-7b22-11e9-8bcf-84061d8a8dc9.png)

grant_type=authorization_code&redirect_uri=http%3A%2F%2Flocalhost%3A8080%2Ffacebookapp%2Fcallback&client_id=447467986082418&code=AQCPK2oPP0jNwNdWixP29lr9DzPTpVaFhJxa4I61VGUIx6mq5z9WpO_tXL5qTx6E2vkj1w53_hOUZrdghCOieK7ysQfD59NzfLTcO8Bxs_vhzMV73uAwls2SqR2IpN1Yzcu1BeS2bdI4zUqoDLt-utUmKrmXD-iw58XpYDrr06_acl7kVo112UdgsTWNrYBNXsYDx1GVCI53B45nqoEJYgtMdsngQV_1swNjvx2cdCIztyt5DvqFBk6ntVCY26Ag3FiYD0QipBTQOxfW1StSXO-tC_USWnAvG2mwV5rBHuqRCDuQiX_Ke6vuq-lzTjqVpe4#_=_

3.6 Get user acess token for your app.

![image](https://user-images.githubusercontent.com/50174329/58027969-5d491880-7b37-11e9-8196-ced2900855cf.png)

3.7 Select the app you have created.
![image](https://user-images.githubusercontent.com/50174329/58028063-91243e00-7b37-11e9-9e8d-895236284913.png)

3.8 Get access token and select the required permission.

![image](https://user-images.githubusercontent.com/50174329/58028531-903fdc00-7b38-11e9-9f72-bc4a1483e0aa.png)

![image](https://user-images.githubusercontent.com/50174329/58028636-d006c380-7b38-11e9-9041-5f14b6c7b031.png)

![image](https://user-images.githubusercontent.com/50174329/58028966-4c010b80-7b39-11e9-825c-a0ebc8225540.png)

![image](https://user-images.githubusercontent.com/50174329/58029122-95515b00-7b39-11e9-9dea-cb426476244f.png)




# djfacebook
Implementing facebook authentication with Django REST framework

# Usage
Clone the project
```
git clone https://github.com/ricardochaves/djfacebook.git
```

Install the packages
```
pip install -r requirements.txt
```

Include the key and the secret of the Facebook API to the ```settings.py```:
```
# Facebook configuration
SOCIAL_AUTH_FACEBOOK_KEY = 'APIKEY'
SOCIAL_AUTH_FACEBOOK_SECRET = 'APISECRET'
```
You can create an API [here](https://developers.facebook.com).


And run
```
python manage.py runserver
```

Now, you can make a post to get a token:
```
curl -X POST -d "grant_type=convert_token&client_id=<client_id>&client_secret=<client_secret>&backend=facebook&token=<facebook_token>" http://localhost:8000/auth/convert-token
```
You can get a user token [here](https://developers.facebook.com/tools/accesstoken/).


# References
Here you can learn more about [django-rest-framework-social-oauth2](https://github.com/PhilipGarnero/django-rest-framework-social-oauth2)

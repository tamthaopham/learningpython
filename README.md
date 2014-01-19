learningpython
==============

# Twitter API

from twython import Twython
twitter = Twython()
APP_KEY = 'CTJlSscgFxUbsSS0rCXPw'
APP_SECRET = '9II53w2wuyIVfblPEzg2q4Ihz9q4iV4hU9ls611t4o'
twitter = Twython(APP_KEY, APP_SECRET)
auth = twitter.get_authentication_tokens()
OAUTH_TOKEN = auth['oauth_token']
OAUTH_TOKEN_SECRET = auth['oauth_token_secret']
t = Twython(APP_KEY, APP_SECRET, OAUTH_TOKEN, OAUTH_TOKEN_SECRET)
user_timeline = twitter.get_user_timeline(screen_name="tamthaopham",)
for tweet in user_timeline:
     print(tweet['text'])


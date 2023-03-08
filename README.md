1/27/23 :
Set up a web server with AWS and a domain

I found it interesting that it costs you the same amount regardless of whether your server is running or not running (at least when using an elastic IP address).

Browser address: http://bookapp.click/

Remote shell command: ssh -i ~/.ssh/260web.pem ubuntu@bookapp.click^C

2/2/23:
Secured web server communication by configuring Caddy to request a certificate from Let's Encrypt for the domain name.

https://bookapp.click/
With the security certificate, the request changed from http -> https

2/6/23 (C4LV1NPU6):
Set up official HTML website.


Website deploy command: ./deployWebsite.sh -k ~/Downloads/260web.pem -h bookapp.click -s startup


2/6/23 :
Set up Simon HTML sub-website.


Sub-site name: https://simon.bookapp.click/

Sub-site deploy command: ./deployFiles.sh -k ~/Downloads/260web.pem -h bookapp.click -s simon

2/10/23:
Made CSS Practice project. Can be used in Startup App's website.


# Design

Are you a book worm? Are you constantly trying to figure out which book to read next? Are you tired of trying to keep up with the pile of new books your grandma sends you for your brithday? Well your solution is here!
Look no further than BookSocial. BC is a great way to keep track of your reading while also connecting with your peers on theirs. You'll be able to 

![image](https://user-images.githubusercontent.com/56054621/215150230-fcd7d947-117e-4cfb-b74c-0e050603bb79.png)

Key Features:

  -Secure login over HTTPS
  -Ability to update book progress as your read
  -Display of choices
  -Ability to research other books
  -Totals from all users displayed in realtime
  -Ability for a user to add freinds to a personal list
  -Ability for a user to check friends personal book progress
  -Ability for admin to create and delete books
  -Ability for user to add future books to wishlist

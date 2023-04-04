# 0x11. Python - Network #1

## Resources
Read or watch:

* [Quickstart with Requests package](https://docs.python.org/3/howto/urllib2.html)
* [Requests package](https://docs.python-requests.org/en/master/)

## Tasks

## [0. What's my status? #0](./0-hbtn_status.py)
  Write a Python script that fetches [https://intranet.hbtn.io/status]

* You must use the package urllib
* You are not allowed to import any packages other than urllib
* The body of the response must be displayed like the following example (tabulation before -)
* You must use a with statement
> ./0-hbtn_status.py | cat -e

## [1. Response header value #0](./1-hbtn_header.py)
  Write a Python script that takes in a URL, sends a request to the URL and displays the value of the [X-Request-Id] variable found in the header of the response.

* You must use the packages [urllib] and [sys]
* You are not allow to import packages other than urllib and sys
* The value of this variable is different for each request
* You don’t need to check arguments passed to the script (number or type)
* You must use a with statement
> ./1-hbtn_header.py https://intranet.hbtn.io

> ./1-hbtn_header.py https://intranet.hbtn.io

## [2. POST an email #0](./2-post_email.py)
  Write a Python script that takes in a URL and an email, sends a POST request to the passed URL with the email as a parameter, and displays the body of the response (decoded in utf-8)

* The email must be sent in the email variable
* You must use the packages urllib and sys
* You are not allowed to import packages other than urllib and sys
* You don’t need to check arguments passed to the script (number or type)
* You must use the with statement
> ./2-post_email.py http://0.0.0.0:5000/post_email hr@holbertonschool.com

## [3. Error code #0](./3-error_code.py)
  Write a Python script that takes in a URL, sends a request to the URL and displays the body of the response (decoded in utf-8).

* You have to manage urllib.error.HTTPError exceptions and print: Error code: followed by the HTTP status code
* You must use the packages urllib and sys
* You are not allowed to import other packages than urllib and sys
* You don’t need to check arguments passed to the script (number or type)
* You must use the with statement
> ./3-error_code.py http://0.0.0.0:5000

> ./3-error_code.py http://0.0.0.0:5000/status_401

> ./3-error_code.py http://0.0.0.0:5000/doesnt_exist

> ./3-error_code.py http://0.0.0.0:5000/status_500

## [4. What's my status? #1](./4-hbtn_status.py)
  Write a Python script that fetches https://intranet.hbtn.io/status

* You must use the package requests
* You are not allow to import packages other than requests
* The body of the response must be display like the following example (tabulation before -)
> ./4-hbtn_status.py | cat -e

## [5. Response header value #1](./5-hbtn_header.py)
  Write a Python script that takes in a URL, sends a request to the URL and displays the value of the variable X-Request-Id in the response header

* You must use the packages requests and sys
* You are not allow to import other packages than requests and sys
* The value of this variable is different for each request
* You don’t need to check script arguments (number and type)
> ./5-hbtn_header.py https://intranet.hbtn.io

> ./5-hbtn_header.py https://intranet.hbtn.io

## [6. POST an email #1](./6-post_email.py)
  Write a Python script that takes in a URL and an email address, sends a POST request to the passed URL with the email as a parameter, and finally displays the body of the response.

* The email must be sent in the variable email
* You must use the packages requests and sys
* You are not allowed to import packages other than requests and sys
* You don’t need to error check arguments passed to the script (number or type)
> ./6-post_email.py http://0.0.0.0:5000/post_email hr@holbertonschool.com

## [7. Error code #1](./7-error_code.py)
  Write a Python script that takes in a URL, sends a request to the URL and displays the body of the response.

* If the HTTP status code is greater than or equal to 400, print: Error code: followed by the value of the HTTP status code
* You must use the packages requests and sys
* You are not allowed to import packages other than requests and sys
* You don’t need to check arguments passed to the script (number or type)
> ./7-error_code.py http://0.0.0.0:5000

> ./7-error_code.py http://0.0.0.0:5000/status_401

> ./7-error_code.py http://0.0.0.0:5000/doesnt_exist

> ./7-error_code.py http://0.0.0.0:5000/status_500

## [8. Search API](./8-json_api.py)
  Write a Python script that takes in a letter and sends a POST request to http://0.0.0.0:5000/search_user with the letter as a parameter.

* The letter must be sent in the variable q
* If no argument is given, set q=""
* If the response body is properly JSON formatted and not empty, display the id and name like this: [<id>] <name>
* Otherwise:
Display Not a valid JSON if the JSON is invalid

Display No result if the JSON is empty

* You must use the package requests and sys
* You are not allowed to import packages other than requests and sys
> ./8-json_api.py

> ./8-json_api.py a

> ./8-json_api.py 2

> ./8-json_api.py b


## [9. My GitHub!](./10-my_github.py)
  Write a Python script that takes your GitHub credentials (username and password) and uses the GitHub API to display your id

* You must use [Basic Authentication]() with a [personal access token]() as password to access to your information (only read:user permission is needed)
* The first argument will be your username
* The second argument will be your password (in your case, a [personal access token]() as password)
* You must use the package requests and sys
* You are not allowed to import packages other than requests and sys
* You don’t need to check arguments passed to the script (number or type)
> ./10-my_github.py papamuziko cisfun

> ./10-my_github.py papamuziko wrong_pwd

## [10. Time for an interview!](./)

```
Please list 10 commits (from the most recent to oldest) of the repository “rails” by the user “rails”
You must use the GitHub API, here is the documentation https://developer.github.com/v3/repos/commits/
Print all commits by: `<sha>: <author name>` (one by line)
```
  Write a Python script that takes 2 arguments in order to solve this challenge.

* The first argument will be the [repository name]
* The second argument will be the [owner name]
* You must use the packages [requests] and [sys]
* You are not allowed to import packages other than requests and sys
* You don’t need to check arguments passed to the script (number or type)
> ./100-github_commits.py rails rails

Be careful: only 60 requests by hour by IP for unauthenticated requests [Rate limit](https://docs.github.com/en/rest)



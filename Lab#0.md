# Lab #0 Prototyping
-----

Lab#0 consists in implementation of a simple prototype application (oAuth service) and analyzing of future application's features, problematic aspects and applications architecture.

## Task #1

Develop an oAuth service which will represent an API with requests:

Request name | Request URL | Input data | Output data | Codes
---|---|---|---|---
Register new user | http://oauthservice/register | {app_id,email,pass,name_surname} | {code,token} | 0,1
Login user | http://oauthservice/login | {app_id,email,user} | {code,token} | 0,2
Get last user login time | http://oauthservice/get_last_login | {app_id,token,email} | {code,time} | 0,3

### Requirements:
- Allow applications to register users.
- Allow applications to login users.
- Allow applications to ask for last login time.
- Allow multiple applications to login/register user at the same time.
- For API will be used http protocol with GET gethod.
- Which language to use is up to you.

Codes description:
Code | Description
---|---
0 | OK
1 | user exists
2 | wrong data
3 | wrong token

Requests example:
```shell
	$curl -o http://127.0.0.1/register?in='{"app_id": "0", "email": "mail@mail.com", "pass": "qwerty", "name_surname": "username"}'
	
	{
		"out": {
			"code": 0
			"token": "FOWEPM"
		}
	}

	$curl -o http://127.0.0.1/register?in='{"app_id": "0", "email": "mail@mail.com", "pass": "qwerty", "name_surname": "username"}'
	
	{
		"out": {
			"code": 1
		}
	}
```

Push resulting application to a github repository.

## Task #2

Analyse in a free form text (you can attach a markdown or other type file to your repository) what will be future difficulties in design and implementation of this app. Another question is "Is this application useful and if not, how I can make it so?".

So you have to define to lists of features. First list will contain technical tasks implemented in order to develop a well working version of current application. Second one is about which features to add to this app in order to get a better version of this app.

Example:
```
	Task: Implement ADD function.

	Realization in pseudocode:
		function ADD (first digit, second digit) -> result digit {
			return digit of first digit + second digit;
		}

	Technical Issues:
		- Result of ADD operation cannot be more than 9. Otherwise value will overfill return variable because it is digit type of. Solution: to use number type for return value.

	Improvement features:
		- ADD function operates with digit arguments only for now. Proposal: change arguments type to number.

```

## Lab #0 work application

To send into this [form](http://goo.gl/forms/B9eQeABa5m)

## Deadline for application is september 21st.

# Have a nice day ;)
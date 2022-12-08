# LinkedIn Email Scraper
A python class that can scrape LinkedIn profiles for emails.

# Prerequisites
1. Python any version
2. Installation of below module using command
<pre>pip install requests</pre>
3. Account in LinkedIn for accessing private profiles

# Usage
Refer to <a href='https://github.com/SecretSanta007/LinkedIn-Email-Scraper/blob/master/demo.py'>demo.py</a> for usage reference. You can modify it as you like. You can import the linkedin.py class file or modify it as per your needs.

This code appears to be a class for interacting with LinkedIn. It contains three methods: __init__, login, bulkScan, and singleScan. The __init__ method sets up a Session object and some headers for making requests. The login method logs in to LinkedIn with a provided email and password. The bulkScan and singleScan methods retrieve email addresses from LinkedIn profiles.

To use this class, you would first need to create an instance of the LinkedIn class. Then, you could call the login method with your email and password to log in to LinkedIn. Once logged in, you could call the bulkScan or singleScan methods to retrieve email addresses from LinkedIn profiles. 

Here is an example:

```
# create an instance of the LinkedIn class
linkedin = LinkedIn()

# log in to LinkedIn
linkedin.login("myemail@gmail.com", "mypassword")

# retrieve email addresses from a list of LinkedIn profiles
profiles = ["https://www.linkedin.com/in/johndoe/", "https://www.linkedin.com/in/janedoe/"]
emails = linkedin.bulkScan(profiles)
print(emails)

# retrieve email addresses from a single LinkedIn profile
email = linkedin.singleScan("https://www.linkedin.com/in/johndoe/")
print(email)

# Example Code For Guest Access
<pre>client = LinkedIn()<br>
client.singleScan(url_to_profile)</pre>
```

To use this class, you would need to have the requests and re modules installed in your Python environment. You can do this by running pip install requests and pip install re in your command line.

To create an instance of the LinkedIn class, you would use the following code:
```
# create an instance of the LinkedIn class
linkedin = LinkedIn()
```
To log in to LinkedIn, you would need to call the login method and provide your email and password as arguments, like this:
```
# log in to LinkedIn
linkedin.login("myemail@gmail.com", "mypassword")
```
Once you are logged in, you can use the bulkScan method to retrieve email addresses from a list of LinkedIn profiles. You would need to provide a list of LinkedIn profile URLs as an argument to the bulkScan method, like this:

```
# retrieve email addresses from a list of LinkedIn profiles
profiles = ["https://www.linkedin.com/in/johndoe/", "https://www.linkedin.com/in/janedoe/"]
emails = linkedin.bulkScan(profiles)
print(emails)
```
Alternatively, you can use the singleScan method to retrieve email addresses from a single LinkedIn profile. You would need to provide the URL of the LinkedIn profile as an argument to the singleScan method, like this:

```
# retrieve email addresses from a single LinkedIn profile
email = linkedin.singleScan("https://www.linkedin.com/in/johndoe/")
print(email)
```
You can also use the class without logging in to LinkedIn, by using the singleScan method with a public LinkedIn profile URL. For example:

```
# create an instance of the LinkedIn class
linkedin = LinkedIn()

# retrieve email addresses from a single LinkedIn profile
email = linkedin.singleScan("https://www.linkedin.com/in/johndoe/")
print(email)
```

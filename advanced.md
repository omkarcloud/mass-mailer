## 🤔 Advanced Questions

### ❓ How to Get Emails Received After a Certain Date?
To get emails from a certain date onwards, use the `received` parameter. 

For example, to get emails after January 1st, 2023 (UTC):

```python
username = "username123"
after = "2023-01-01"
Outlook.get_emails(username, received=after)
```

### ❓ How to Get a Maximum of 10 Emails?
To limit your email retrieval to 10, use the `max` parameter:

```python
username = "username123"
Outlook.get_emails(username, max=10)
```
This fetches the 10 most recent emails in your inbox.

### ❓ How to Get Unread Emails?
To collect all unread emails, use the `Outlook.get_unread_emails` method:

```python
username = "username123"
unread_emails = Outlook.get_unread_emails(username)
print(unread_emails)
```
Note: This action marks unread emails as read.

### ❓ How to Get Spam Emails Along with Primary Emails?
To get both primary and spam emails, set the `with_spam` parameter to `True`:

```python
username = "username123"
emails = Outlook.get_emails(username, with_spam=True)
print(emails)
```

### ❓ How to Use Proxies for Account Creation?
We suggest using a mobile hotspot over proxies for these reasons:
1. **Faster, More Stable Internet:** Mobile hotspots offer better speed and stability.
2. **Simpler Captchas:** Captchas are easier with mobile hotspots.
3. **Cost-Effective:** Mobile hotspots are free; proxies can be expensive.

However, if you prefer proxies, here's how to implement them:

```python
proxies = [
    "http://myusername1:mypassword@myproxy-provider.com:8080",
    "http://myusername2:mypassword@myproxy-provider.com:8080",
]
Outlook.create_accounts(count=4, proxies=proxies)
```
We will rotate the proxies automatically.

### ❓ Which Proxy Provider to Choose?

#### For Account Creation:
Currently, manual account creation is recommended as popular proxies like Bright Data and IPRoyal refuses to connect for signup urls. 

However, if you know of any Proxy Provider that works for creating Outlook Accounts, please let us know in the Github Discussions [here](https://github.com/omkarcloud/mass-mailer/discussions), and we will add them to the list. This will help you earn Good Karma.

#### For Getting/Sending Emails:

During our testing, IPRoyal worked well for getting/sending emails. Avoid using Bright Data as it refuses to connect.


### ❓ Why did you use Firefox for Account Creation instead of Chrome?

Chrome was getting detected, and we were facing the following problems:

- Captchas were much harder and longer to solve (10 steps long).
- Even after successfully solving the Captcha, we were asked to solve it again and again in a loop.

So, we used Firefox, which doesn't cause these issues, and Captchas are much easier to solve.

### ❓ How to Use Captcha Solvers like Capsolver and 2Captcha for Automatically Solving Captchas?

We attempted to use various captcha solvers like Capsolver, 2Captcha, and 1stCaptcha, but none of them worked.

Finally, we found a [Capsolver Chrome Extension](https://chromewebstore.google.com/detail/captcha-solver-auto-bypas/pgojnojmmhpofjgdmaebadhbocahppod) that successfully solved the captcha.

Unfortunately, the extension is not available on Firefox. We are waiting for the Capsolver team to release a Firefox extension (as mentioned on their [Chrome Web Store page](https://chromewebstore.google.com/detail/captcha-solver-auto-bypas/pgojnojmmhpofjgdmaebadhbocahppod)). Once it's released, we will update the tool to use it, allowing you to solve captchas automatically.

In the meantime, you will have to manually solve captchas. You can check back on this repository in three months to see if the Firefox extension has been released.

### ❓ I am an experienced Web Scraper and can integrate Captcha Solving in Bot, where to start?

Follow these steps to get started with Captcha Solving Integration:

1.  Enable Captcha Solving by using the following code:
```python
Outlook.create_accounts(enable_captcha_solving=True)
```
2.  Implement the `solve_captcha` function in the `solve_captcha.py` file and make sure it returns the Captcha Token.
3.  If case, you are successful in solving the Captcha, please share your solution in the Github Discussions [here](https://github.com/omkarcloud/mass-mailer/discussions).


### ❓ Is the Tool Safe for Account Creation?
Absolutely. It's trusted by thousands of developers globally for creating Outlook accounts.

### ❓ Can the Tool Be Used for Spam or Malicious Activities?
No. It's meant for legitimate uses like business, testing, and personal accounts. Misuse for spam or malicious acts is against our and Microsoft's policies.


### ❓ What is the Difference Between your mass-mailer and outlook-account-generator?

Both repositories use the same web scraper but are tailored for different audiences:

**omkarcloud/mass-mailer:** 
- Its README focuses on Mass Mailing.

**omkarcloud/outlook-account-generator:** 
- Its README focuses on Outlook Account Generation for signing up on websites.

**Choose based on your need:**
- Bulk Mailing ➡️ `mass-mailer`, as its README is written specifically for your use case.
- Outlook Account Generation for signing up on websites ➡️ `outlook-account-generator`, as its README is written specifically for your use case.


Note: Both repositories are exactly same in terms of code and functionality. The only difference is the README.
### ❓ Need More Help or Have Additional Questions?

For further help, ask your question in GitHub Discussions. We'll be happy to help you out.

[![ask github](https://raw.githubusercontent.com/omkarcloud/google-maps-scraper/master/screenshots/ask-on-github.png)](https://github.com/omkarcloud/outlook-account-generator/discussions)



## Love It? [Star It ⭐!](https://github.com/omkarcloud/mass-mailer)

Become one of our amazing stargazers by giving us a star ⭐ on GitHub!

It's just one click, but it means the world to me.

[![Stargazers for @omkarcloud/mass-mailer](https://bytecrank.com/nastyox/reporoster/php/stargazersSVG.php?user=omkarcloud&repo=mass-mailer)](https://github.com/omkarcloud/mass-mailer/stargazers)

## Made with ❤️ using [Botasaurus Web Scraping Framework](https://github.com/omkarcloud/botasaurus)
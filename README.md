![Mass Mailer Featured Image](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/mass-mailer-scraper-feautred-img.png)

<div align="center" style="margin-top: 0;">
  <h1>🚀 Mass Mailer 📧</h1>
  <p>💦 Send Bulk Mails 💦</p>
</div>
<em>
  <h5 align="center">(Programming Language - Python 3)</h5>
</em>
<p align="center">
  <a href="#">
    <img alt="mass-mailer forks" src="https://img.shields.io/github/forks/omkarcloud/mass-mailer?style=for-the-badge" />
  </a>
  <a href="#">
    <img alt="Repo stars" src="https://img.shields.io/github/stars/omkarcloud/mass-mailer?style=for-the-badge&color=yellow" />
  </a>
  <a href="#">
    <img alt="mass-mailer License" src="https://img.shields.io/github/license/omkarcloud/mass-mailer?color=orange&style=for-the-badge" />
  </a>
  <a href="https://github.com/omkarcloud/mass-mailer/issues">
    <img alt="issues" src="https://img.shields.io/github/issues/omkarcloud/mass-mailer?color=purple&style=for-the-badge" />
  </a>
</p>
<p align="center">
  <img src="https://views.whatilearened.today/views/github/omkarcloud/mass-mailer.svg" width="80px" height="28px" alt="View" />
</p>

---

⚡ Send Mass Mails! ⚡

👋 Hello, I am the Mass Mailer, a powerful tool designed to automate the process of sending bulk emails. 

If you've experienced disappointments with other mass mailing bots, facing failures, crashes and detection, don't worry! Your search for a reliable Mass Mailer ends right here ⬇️.


## ⚡ Features and Benefits

1. **Unlimited Mass Mails for Free**
2. **Realistic Account Names:** Accounts are created with human-like names, reducing the chances of getting banned.
3. **Easy Email Sending and Receiving:** *Send* and *receive emails* with just one line of code.

Ready to Rock n Roll? Let's get started!

## 🎥 Video Demo

Watch this video to see the bot in action!

[![Mass Mailer](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/youtube-video.png)](https://www.youtube.com/watch?v=RwCWcaKBahI)

## 🚀 Getting Started

1️⃣ **Clone the Magic 🧙‍♀:**
   ```shell
   git clone https://github.com/omkarcloud/outlook-account-generator mass-mailer
   cd mass-mailer
   ```
2️⃣ **Install Dependencies 📦:**
   ```shell
   python -m pip install -r requirements.txt
   ```
3️⃣ **Let the Rain of Outlook Accounts Begin 😎:**
   ```shell
   python main.py
   ```

The bot will take care of filling in the required details automatically. You will only be prompted to solve the captcha manually.

![solve captcha](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/solve-captcha.png)

Note:
  1. Accounts will be saved in `profiles.json`.
  ![Outlook Account](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/profiles.png)

  2. This Bot requires Firefox, as firefox is able to bypass Microsoft's Anti-Detection Measures. If you don't have Firefox, download it from the Mozilla website [here](https://www.mozilla.org/en-US/firefox/new/).
  

## 🤔 FAQs

### ❓ How to Change the Number of Accounts to Create?
By default, the bot creates 1 account.

To create more accounts, open the `main.py` file and update `Outlook.create_accounts` by adding the `count` parameter. 

This parameter specifies the number of accounts to be created:

```python
Outlook.create_accounts(count=3)
```

The above code will create 3 accounts.

### ❓ How Many Accounts Can I Create?
The sky's the limit! However, Outlook will prompt you for phone verification after every 3 accounts.

![Photo Verification](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/phone-verification.png)


But don't worry! Bypassing the photo verification prompt is very easy. All you need to do is change your IP address.

While there are numerous ways to change your IP, such as using VPNs and proxies, we'll share with you the **fastest**, **simplest**, and best of all, the **free** way which is as follows:

1. **Connect your PC to the Internet via a Mobile Hotspot.**
2. **Toggle airplane mode off and on on your mobile device.** This will assign you a new IP address.
3. **Turn the hotspot back on.**

Please note that you need to repeat this process after every 3 accounts. We will automatically prompt you when it's needed like so.

![Prompt Image](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/prompt-image.png)

### ❓ How to View All Created Accounts?

You can view the accounts you have created in **`profiles.json`**.

![Outlook Account](https://raw.githubusercontent.com/omkarcloud/mass-mailer/master/images/profiles.png)

Additionally, you can get a list of all created accounts by using `Outlook.get_accounts`:
```python
accounts = Outlook.get_accounts()
print(accounts)
```

### ❓ How to Send Email?

To send an email, you can use the `Outlook.send_email` method. Replace the `to` with your personal email.

```python
username = "username123"

to = "my-email@gmail.com" # For testing, replace with your personal email
subject = "Product Roadmap Discussion"
body = "We will discuss the product roadmap."

Outlook.send_email(username, to, subject, body)
```

After executing this, check your personal email *primary*/*spam* box to see the sent message.

You can also send emails with HTML content. The following example shows how to send an email with a hyperlink embedded in the body:

```python
username = "username123"

to = "my-email@gmail.com" # For testing, replace with your own email
subject = "Meeting Productivity Article"

body = """I recommend reading <a href='https://www.atlassian.com/work-management/project-collaboration/team-meetings'>this article</a> about improving meeting productivity."""

Outlook.send_email(username, to, subject, body)
```

### ❓ How to Send Multiple Emails with It?

To send multiple emails, use the `Outlook.send_emails` method as follows:

```python
username = "username123"

emails = [
  {
    "to": "my-email@gmail.com",
    "subject": "Presentation Preparation",
    "body": "Have you prepared your presentation?"
  },
  {
    "to": "my-email2@gmail.com",
    "subject": "Rescheduled Meeting",
    "body": "Our meeting has been rescheduled to Wednesday."
  }
]

Outlook.send_emails(username, emails)
```

This method will automatically insert a random delay between each email to make the sending process appear more human-like and avoid account suspension.


### ❓ How to get all Emails?

Use `Outlook.get_emails` to get all the emails:

```python
username = "username123" 
Outlook.get_emails(username)
```

### ❓ How to Get Emails Received 1 Day/1 Week Ago?

To get emails a specific timeframe ago, use the `received` parameter.

For example, to get emails received 1 week ago, use the following code:

```python
username = "username123"
ago = Outlook.Ago.OneWeekAgo
Outlook.get_emails(username, received=ago)

```

Some popular options for the `received` parameter are:
- Outlook.Ago.TwoMinutesAgo
- Outlook.Ago.OneHourAgo
- Outlook.Ago.OneDayAgo
- Outlook.Ago.OneWeekAgo
- Outlook.Ago.OneMonthAgo
- Outlook.Ago.OneYearAgo

See the list of all supported timeframes [here](https://github.com/omkarcloud/mass-mailer/blob/master/agos.md)

### ❓ How to Manually Open the Outlook Website for an Account?

To manually open the Outlook website for a specific account to review emails, use the `Outlook.open` method as follows:

```python
username = "username123" # Replace with your username found in profiles.json
Outlook.open(username)
```

After running, the specified Outlook account will be open in `outlook.live.com`. You will then be prompted to press Enter once you have finished reviewing your emails.


### ❓ What precautions should be followed to avoid getting banned while sending and receiving emails?

1. Use different IP addresses for each email account by using rotating residential proxies. 

Also ensure that the proxy's country matches the account's creation country. 

You can use pass proxies as follows:
```python
Outlook.send_email(username, to=to, subject=subject, body=body, proxy="http://username:password@ip:port")
Outlook.get_latest_email(username, proxy="http://username:password@ip:port")
```
2. Personalize your emails. Include the recipient's name and company in the subject and body.

3. Avoid sending excessive emails from a single account, as this can trigger the phone verification process. Instead distribute the email load across multiple accounts.

### ❓ Do you have any recommendations on how many emails to send per day?

1. Limit to 9 emails per account daily. This allows for approximately 10,800 emails per month with 40 accounts (40 accounts x 9 emails/day x 30 days).

2. If more emails are needed, add extra accounts. For example, to send an additional 1,000 emails per month, create 4 more accounts.

3. For better email deliverability, it's recommended to send fewer emails per account and add more accounts if necessary.

### ❓ Advanced Questions

Having read this page, you have all the knowledge needed to effectively utilize the bot and send mass mails.

You may choose to explore the following questions based on your interests:

#### For Technical Usage

1. [How to Get Emails Received After a Certain Date?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-get-emails-received-after-a-certain-date)
2. [How to Get a Maximum of 10 Emails?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-get-a-maximum-of-10-emails)
3. [How to Get Unread Emails?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-get-unread-emails)
4. [How to Get Spam Emails Along with Primary Emails?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-get-spam-emails-along-with-primary-emails)
5. [How to Use Proxies for Account Creation?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-use-proxies-for-account-creation)

#### For Knowledge

1. [Which Proxy Provider to Choose?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-which-proxy-provider-to-choose)
2. [Why did you use Firefox for Account Creation instead of Chrome?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-why-did-you-use-firefox-for-account-creation-instead-of-chrome)
3. [How to Use Captcha Solvers like Capsolver and 2Captcha for Automatically Solving Captchas?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-how-to-use-captcha-solvers-like-capsolver-and-2captcha-for-automatically-solving-captchas)
4. [I am an experienced Web Scraper and can integrate Captcha Solving in Bot, where to start?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-i-am-an-experienced-web-scraper-and-can-integrate-captcha-solving-in-bot-where-to-start)
5. [Is the Tool Safe for Account Creation?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-is-the-tool-safe-for-account-creation)
6. [Can the Tool Be Used for Spam or Malicious Activities?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-can-the-tool-be-used-for-spam-or-malicious-activities)
7. [What is the Difference Between your mass-mailer and outlook-account-generator?](https://github.com/omkarcloud/mass-mailer/blob/master/advanced.md#-what-is-the-difference-between-your-mass-mailer-and-outlook-account-generator)

### ❓ Need More Help or Have Additional Questions?

For further help, ask your question in GitHub Discussions. We'll be happy to help you out.

[![ask github](https://raw.githubusercontent.com/omkarcloud/google-maps-scraper/master/screenshots/ask-on-github.png)](https://github.com/omkarcloud/outlook-account-generator/discussions)



## Love It? [Star It ⭐!](https://github.com/omkarcloud/mass-mailer)

Become one of our amazing stargazers by giving us a star ⭐ on GitHub!

It's just one click, but it means the world to me.

[![Stargazers for @omkarcloud/mass-mailer](https://bytecrank.com/nastyox/reporoster/php/stargazersSVG.php?user=omkarcloud&repo=mass-mailer)](https://github.com/omkarcloud/mass-mailer/stargazers)

## Made with ❤️ using [Botasaurus Web Scraping Framework](https://github.com/omkarcloud/botasaurus)

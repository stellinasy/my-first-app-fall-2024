# my-first-app-fall-2024

## Setup

Create a virtual environment (first time only):

```sh
conda create -n reports-env-2024 python=3.10
```

Activate the environment (whenever you come back to this project):

```sh
conda activate reports-env-2024
```

Install packages:

```sh
pip install -r requirements.txt
```
[Obtain an API Key](https://www.alphavantage.co/support/#api-key) from AlphaVantage.

Create a ".env" file and add contents like the following (using your own AlphaVantage API Key):

```sh
# this is the ".env" file:
ALPHAVANTAGE_API_KEY="..."
```

Set up email sending service (Mailgun):

To use Mailgun for sending email, you must first follow some setup instructions to create an account, verify your account, setup a sandbox domain, then finally obtain an API Key.

+ Create a Mailgun account with your business or university email address (i.e. MAILGUN_SENDER_ADDRESS). Click the verification link sent to that address.
+ Login. Find and click the nav link about "Sending" email. From the domains page, note the sandbox domain provided to you by default (i.e. MAILGUN_DOMAIN like "sandbox-xyz.mailgun.org").
+ Find and click on API Key settings link on bottom right, then on the API Keys page, scroll down and click the button to create a new API Key (i.e. MAILGUN_API_KEY).

+ NOTE: Sandbox domains are restricted to authorized recipients only. So you'll only be able to send emails to yourself and a handful of "beta tester" friends and family until / unless you register your own domain later.
+ NOTE: if you see 403 error later, try registering your own email address as an "Authorized Recipient", and click the verification email, and try again


## Usage 

Run the example script:

```sh
python app/my_script.py
```

Run the unemployment report:

```sh
#ALPHAVANTAGE_API_KEY="..." python app/unemployment.py

python app/unemployment.py
```

Run the stocks report:

```sh
python app/stocks.py
```

Run the example email sending file:
```sh
python app/email_service.py
```

Run the RPS game:
```sh
python app/rps.py
```
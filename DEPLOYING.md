# Deploying to Render

Follow this guide if you would like to deploy your host your application on a free server provided by the Render platform.

References:
  + https://render.com/docs/deploy-flask

## Render Setup
Login to [Render](https://dashboard.render.com) and visit the dashboard.

Create a New "Web Service". Choose your own repository by specifying its public URL (at the bottom of the page).

Specify start command:
```
gunicorn "web_app:create_app()"
```

Choose instance type of "free".

Under the "Advanced" options, set an environment variable called `ALPHAVANTAGE_API_KEY` (specifying your own API Key value, without quotes). Also set an environment called `SECRET_KEY` and specify your own unique value.

Finally, click to "Create" the web service.
# Simple webhook for DialogFlow using ngrok

This is a simple web hook for DialogFlow.

Install it by cloning this repo and change into it and run: `npm install`.

To start [ngrok](https://ngrok.com/) & the Express server run: `npm run server`

To see your ngrok server endpoint head over to : `http://localhost:4040`

Use the address you see above and add **silly** at the end: `https://<YOUR-ngrok>/silly` - this is the webhook endpoint to add in DialogFlow.

Enjoy!

## Gotchas

* The webhook is a POST request.
* Printing out the `req.body` helps you to see what the DialogFlow send to the webhook.
* The web hook should return a JSON object that looks like this:
```json
{
  "speech" : "speech response",
  "displayText" : "text response here"
}
```

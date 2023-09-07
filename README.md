# PostToNostrFromAlgia
 Create Webhook : Post to Nostr From algia on Linux Server
Using Python.
Create a webhook on a Linux server to post to Nostr.

The prerequisite is that algia (https://github.com/mattn/algia) is running.
The system is designed to start algia running on a Linux server.

The config.json in the repository is not for this project, but is the recommended config for algia.

When PostToNostr.py is executed, it becomes a webhook that starts with "http:<yourdomain>:5000/webhook".

In the Post action to the webhook.
{ "id-key" : "test-key", "text" : "string to be POSTed" }
and the JSON
"Content-Type: application/json" and POST it via HTTP with the Content-Type.

To actually use it, change "/webhook" in PostToNostr.py to your favorite access URL, "port:5000" to your favorite port when changing the port, and ""test-key"" to change the access key.
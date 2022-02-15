# :package: GitHub Manager

We are developing our own repository management bot on the GitHub platform.

## How does it work?

[Read the official GitHub documentation](https://docs.github.com/en/developers/webhooks-and-events/webhooks/about-webhooks)

!!!success You can use our solutions!
The project is open-source. You can use it on your own Discord server, or anywhere else
!!!

## How to use
### Create GitHub webhook
1. Go to repo => Settings => Webhooks
2. Create:

![Repository settings - Webhooks](https://cdn.upload.systems/uploads/1yLzQP12.png)
!!!danger Use Client Secret!
If you want your webhook to be secure, enter your own clientSecret to secure your data
!!!

![Webhook settings](https://cdn.upload.systems/uploads/QZKcljlA.png)
### Run the server
1. Download repo https://github.com/Skyndalex/github-manager
2. Unzip files
3. replace channelID string to your channel ID
```js 
const channelID = "924792134702366750" 
```
3. Run the server - `node github.js`

!!! warning
Now you can only use the functions that are listed on this trello tab - [View](https://trello.com/c/eLXjsiW8/12-github-manager)
!!!

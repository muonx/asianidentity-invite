How To Make Changes To hackogden.com
------------

1. Make sure NodeJS is installed on your machine: [https://nodejs.org/](https://nodejs.org/)
2. Make sure git is installed on your machine: [https://git-scm.com/](https://git-scm.com/)
3. In terminal navigate to the directory on your computer where you want to download the website files `cd path/to/directory`
4. Run `git clone git@github.com:hackogden/hackogden.com.git`
5. Navigate into the project directory: `cd hackogden.com`
6. Run `npm install` to install site dependencies
7. Run `npm start` to startup a node server on your machine.
8. Preview the site on your local machine at: [http://localhost:3000](http://localhost:3000)
9. Make changes to your heart's desire!
10. When done commit your changes with git and watch the Heroku magic happen!


Slack Invite Automation
------------

A tiny web application to invite a user info your slack team.

Inspired by
[How I hacked Slack into a community platform with Typeform](https://levels.io/slack-typeform-auto-invite-sign-ups/)
and
[Socket.io's slack page](http://socket.io/slack/).

[![Deploy to Heroku](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy)

## Setting
fill out `config.js` as your infomation.

* `community`: your community or team name to display on join page.
* `slackUrl` : your slack team url (ex: socketio.slack.com)
* `slacktoken` : access token of slack.
  You can generate it in <https://api.slack.com/web#auth>

  You can test your token via curl:

  ```shell
   curl -X POST 'https://YOUR-SLACK-TEAM.slack.com/api/users.admin.invite' \
   --data 'email=EMAIL&token=TOKEN&set_active=true' \
   --compressed
  ```

## Run
[Node.js](http://nodejs.org/) is required.

```shell
$ git clone git@github.com:outsideris/slack-invite-automation.git
$ cd slack-invite-automation
$ npm install
$ bin/www
```

You can access <http://localhost:3000> on your web browser.

![](https://raw.github.com/outsideris/slack-invite-automation/master/screenshots/join-page.png)

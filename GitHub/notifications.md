# :receipt: Notifications

Things built into the code:

## Todo:

- [ ] Deployements
- [ ] Discussions
- [ ] Projects
- [ ] Project cards
- [ ] Team
- [ ] Team add
- [x] Stars
- [ ] Pull request reviews
- [ ] Forks
- [ ] Project create
- [ ] Project close
- [ ] Pull requests
- [x] Issues
- [x] Issues comments
- [x] Commits
- [x] Commit comments
- [x] Discussion comments
- [x] Pull request review comments

## Customizing

1. go to file `github-manager/src/webhook/server.js`
2. Edit embed

```js
let embed = new MessageEmbed()
.setAuthor({name: sender.login, iconURL: sender.avatar_url})
.setTitle(`(${repository.full_name}) New commits [${commitList.length}]`)
.setDescription(`**${commitList.join(",\n")}**`)
.addField(`Modified file(s)`, `\`${head_commit.modified.join(",\n") || "None"}\``, true)
.setURL(`https://github.com/Skyndalex/github-manager/commit/${after}`)
.setColor(`GREEN`)
await client.channels.cache.get(channelID).send({embeds: [embed]})
```

!!!success
You can get `JSON` response with creating any action in the repository/organization.

You must have a line `console.log(body)` under the line
```js
const { commits, head_commit, pusher, pull_request, issue, comment, repository, after, sender } = body;
```
!!!
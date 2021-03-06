![Backstroke](https://backstroke.us/assets/img/logo.png)
Backstroke
===
A Github bot to keep a fork updated with any changes made to its upstream.
Heavily inspired by Greenkeeper.

[![Build Status](https://travis-ci.org/1egoman/backstroke.svg?branch=master)](https://travis-ci.org/1egoman/backstroke)
[![Gratipay Team](https://img.shields.io/gratipay/team/Backstroke.svg?maxAge=2592001)](https://gratipay.com/Backstroke/)
[![Website](https://img.shields.io/website-up-down-green-red/http/backstroke.us.svg?maxAge=2592000)](https://backstroke.us)

[![Support via Gratipay](https://cdn.rawgit.com/gratipay/gratipay-badge/2.3.0/dist/gratipay.svg)](https://gratipay.com/Backstroke/)

## Add Backstroke to a repository

1. Go to [backstroke.us](https://backstroke.us), and sign in with your Github account.
2. Click `Create new link`
3. Add a source repo under the text `From` (the big, green box)
4. Add a destination repository under the text `To`, or choose `All Forks` to
   sync to all forks of the source repo.
5. Click `Save`. If you push a change to the repo listed under `From`, you'll
   get a pull request with any updates in the repo(s) under `To`!

### Use Backstroke classic
Backstroke classic is no longer the recommended way to set up Backstroke,
however, if you'd prefer to live with a few limitations, it's still available.

1. Create a webhook in either a fork or a upstream repository. (`Settings` => `Webhooks & Services` => `Add Webhook`)
2. Add `http://backstroke.us` as the payload url.
3. Create the webhook, and push some code to the upstream repository to see Backstroke in action.

## How it works
![How Backstroke Works](public/assets/img/map.png)

### For a contributor
1. You push code to Github.
2. Backstroke will create a pull request with any unmerged upstream changes.
3. You accept Backstroke's pull request, and have updated code. Merging your
   code back upstream later on is painless.

### For an open source maintainer
1. You get a pull request from a contributor.
2. Backstroke will create a pull request on their fork that lets them merge in
   your upstream changes.
3. They accept Backstroke's pull request, and you merge in their code.

<!--
## Advanced Usage
- `upstream`: A string following the format `user/repo` corresponding to a
  custom upstream to merge from into a fork. For example, adding a webhook on a
  fork with `http://backstroke.us/?upstream=foo/upstream` will create a pull
  request (on the fork) that merge in new changes from the custom upstream
  (`foo/upstream`).
-->

## FAQ
- **I don't see any pull requests on the upstream....**: Pull requests are
  always proposed on forks. Take a look there instead.

- **I didn't sign up for this and now I'm getting pull requests. What's going
  on?**: This is because the upstream added backstroke to their repository.
  Some project maintainers use backstroke as an easy way to keep contributor's
  local forks up-to-date with later changes, but if you'd rather tackle that
  unassisted, here's how to [disable backstroke on a fork](./public/assets/disable-on-a-fork.md).

- **Why isn't Backstroke working?**: Take a look at the webhook response logs. Most likely, you'll see an error. Otherwise, open an issue.

- **Is Backstroke really all that useful?**: If you never merge upstream, then no, not really. Otherwise, if you hate
resolving merge conflicts, then it's great.

- **Does Backstroke work outside of Github?**: Not yet. If there's interest, I'd love to give it a try, though.

-------
By [Ryan Gaus](http://rgaus.net)

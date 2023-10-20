# Github Actions Trigger Telegram

A project which would trigger a CI/CD Pipeline in the GitHub Actions upon pushing a commit.

## Steps Taken

1. Fork Uli's DevOps Course [Repo]([url](https://github.com/u1i/ghactions-test)https://github.com/u1i/ghactions-test)
2. In the Github repo, go to Settings > [Pages]([url](https://github.com/Drakeral/ghactions-tele-trigger/settings/pages)) and update the Branch to master and save. This will enable the CI/CD pipeline in Github and to trigger a build each time a commit to the master branch is made
3. Implement Webhooks IFTTT to connect to Telegram ([How to implement webhooks]([url](https://hevodata.com/learn/ifttt-webhook/#:~:text=Users%20can%20implement%20a%20Webhook,Webhooks%20using%20simple%20Web%20Requests)https://hevodata.com/learn/ifttt-webhook/#:~:text=Users%20can%20implement%20a%20Webhook,Webhooks%20using%20simple%20Web%20Requests))
4. Follow the steps on Telegram to successfully integrate the IFTTT bot into the newly created Telegram channel/group
5. Go to the [IFTTT]([url](https://ifttt.com/maker_webhooks)) webhook page and click on the documentation to get a unique IFTTT Webhook URL
6. Update the CURL in the manifest.yml file with the one copied from the documentation
7. Commit changes to test if the CI/CD pipeline is being triggered in the GitHub Actions

## Challenges Faced

- I was unable to generate the Extra Data. Is it showing {{JsonPayload}}
- Took a long time to integrate to IFTTT. Small details such as including the {event} in the curl request of the manifest.yml
- Added a seperate IFTTT bot into my own group chat. This is dangerous as we are giving admin permission to a stranger in the group chat we are creating

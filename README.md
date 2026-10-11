# esp home

My esp home stuff

# git sync

I want to use the [Version history](https://github.com/esphome/device-builder/blob/main/README.md#version-history) of esphome while also doing my own stuff with git.

To set this up:

1. Install an configure "Terminal & SSH" App on HA
2. `git remote add ha-esphome root@ha.host:/root/homeassistant/esphome`
3. `get fetch ha-esphome`
4. Then just do the git stuff as needed
5. `git push ha-esphome <branch>`

On the home assistant machine:
1. `cd /root/homeassistant/esphome`
2. `git config receive.denyCurrentBranch warn`

This allows to push to the current checked out branch which will required a
`git reset --hard` on the home assistant box to update the current branch.

This is somewhat dangerous 🐉

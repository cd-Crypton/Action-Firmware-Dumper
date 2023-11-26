## Action Firmware Dumper

Firmware Dumper using DumprX Source Code Script. This workflows will let you dump in your own GitLab Account/Organization.

## Pre-requisites

* GitLab Account: Setup your Access Token, and make a copy of your token name and the token key itself.
* Fork this repository.
* Go to Settings of the forked repository.
* Then go to Secrets and Variables, and tap Action in dropdown choices.
* Tap New Repository Secrets;
   * Add this:
      * `GITLAB_TOKEN_NAME`
      * `<paste here your token name>`
   * Then tap Add Secrets.
* Tap New Repository Secrets, again;
   * Add this:
      * `GITLAB_TOKEN`
      * `<paste here your access token>`
   * Then tap Add Secrets.

## Notes
* Firmware that has split super image as part of ota/payload won't work.
* Blobs/files that size is over 100MB won't work, GitLab has limit per file size.
* Most oplus devices uses generic name "ossi" in build.prop of system, vendor and even in product partition, only odm partition has the right device model/name. If device dump end up having ossi name, don't get confused whether you made a wrong dump or not.

## Action Firmware Dumper

Firmware Dumper using DumprX Source Code Script. This workflows will let you dump in your own GitLab Account/Organization. It is a bit slower compare to other CI/CD, but it works as fine.

## Pre-requisites

* GitLab Account: Setup your Access Token, and make a copy of your token name and the token key itself.
* Fork this repository.
* Go to Settings of the forked repository.
* Then go to Secrets and Variables, and tap Action in dropdown choices.
* Tap New Repository Secrets;
   * Add this:
      * `gitlab_tokenName`
      * `<paste here your token name>`
   * Then tap Add Secrets.
* Tap New Repository Secrets, again;
   * Add this:
      * `gitlab_userToken`
      * `<paste here your access token>`
   * Then tap Add Secrets.

## Notes
* Most OPlus-related stock firmware (Realme, for example) doesn't work using because of it not being able to get the build.prop, hence failing.
* Reason is, most of it has split super inside, therefore super.img cannot be extracted, hence no build properties from system, vendor nor product.
* Unless its an OTA firmware, it might work, as most OTA uses payload.bin now, and super image inside wasn't split in multiple files.


# World Humanitarian Day 2021 - Static archive

To make edits, spin up https://github.com/UN-OCHA/whd-site-2021

## Static generation process

Due to some weirdness with [Tome](https://www.drupal.org/project/tome) and oEmbed URLs we ended up using [SiteSucker](https://ricks-apps.com/osx/sitesucker/index.html) to make the copy. Use the following configuration to replicate the Drupal URL structure (e.g. `/ru/` instead of `/ru.html` for Russian homepage):

- Settings > General > Treat Ambiguous URLs as Folders: **enabled**

Afterwards, the following commands were run to clean up all the extra files that got generated:

- `rm -rf _downloads.html front/ index.php/ {ar,es,fr,ru,zh-hans}/front/`
- `rm -rf {learn-more,continue-the-race}/{ar,es,fr,ru,zh-hans}`
- `rm -rf ar/{تابع-السباق,لمزيد-من-المعلومات}/{ar,es,fr,ru,zh-hans}`
- `rm -rf es/{continúe-la-carrera,más-información}/{ar,es,fr,ru,zh-hans}`
- `rm -rf fr/{continuez-la-course,en-savoir-plus}/{ar,es,fr,ru,zh-hans}`
- `rm -rf ru/{продолжайте-гонку,узнайте-больше}/{ar,es,fr,ru,zh-hans}`
- `rm -rf zh-hans/{了解更多,竞速不停}/{ar,es,fr,ru,zh-hans}`
- `rm themes/whd2021/img/whd-logo/whd-white-{ar,es,en,fr,ru,zh-hans}.png,.html`
- `mv robots.ssl.txt robots.txt`

xtuple-linguist
===============

This is where translation files for the xTuple webapp are kept. 

With every release, we augment these files with the latest translatable strings from the app.
We use an [automated service](http://translate.google.com) to do the first pass, and rely on
our community to improve the files from there.

### Contributing

If you are familiar with git, then you'll already know how to contribute. Fork this repo, improve
the translations, and submit a pull request.

Even if you're not technical, you can help improve these files using the web front-end that github
provides.

Step 1: [Sign up](https://github.com/join) for Github.

Step 2: Fork this repo by clicking the `Fork` button in the upper-right-hand corner of this repository's
[home page](https://github.com/xtuple/xtuple-linguist).

Step 3: From your fork's root, navigate into the `translations` folder and click on the dictionary you
want to update. 

Step 4: Update the file and click the green `Commit Changes` button.

Step 5: Now if you go back to your fork's root, you'll see an opportunity to `Compare and Pull Request`
to our main repo. Click this button, and then click to `Send Pull Request`. 

That's it! We'll write back to you if we have any questions or comments about your pull request.

### Using

We intend to automatically build all of our translations into the database, so that no manual 
setup is necessary. Until we do, though, or if you want to use your own translation file, you
can add the file manually.

```
cd /path/to/xtuple
./scripts/import_dictionary -d dev -f ../xtuple-linguist/translations/es_MX_dictionary.js
```

Then, from the `UserAccount` workspace of the mobile client, set your locale to `Spanish` (in
this case) and refresh the browser.

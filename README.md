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

1. [Sign up](https://github.com/join) for Github.

2. Fork this repo by clicking the `Fork` button in the upper-right-hand corner of this repository's
[home page](https://github.com/xtuple/xtuple-linguist).

3. From your fork's root, navigate into the `translations` folder and click on the dictionary you
want to update. 

4. Update the file and click the green `Commit Changes` button.

5. Now if you go back to your fork's root, you'll see an opportunity to `Compare and Pull Request`
to our main repo. Click this button, and then click to `Send Pull Request`. 

That's it! We'll write back to you if we have any questions or comments about your pull request.

### Understanding Context

It will likely be helpful for you to understand the context in which these tags are being used in
the app, because a word might have multiple meanings in different contexts.

The most straightforward way to see the contexts of a tag is to grep the codebase

```
cd /path/to/xtuple
grep -r _abbreviation .
```

An alternate approach is to change your locale to something that we have no strings for, and refresh the browser. You'll now just see the tags as you surf around.

It is sometimes also the case that the core developers, as English speakers, don't realize that two words are different words in other languages because they're the same word in English. Please file an issue in this repository if you'd like us to fork a tag into two tags, each with the same English translation, but with the possibility of a split translation in your language.

### Using

We intend to automatically build all of our translations into the database, so that no manual 
setup is necessary. Until we do, though, or if you want to use your own translation file, you
can add the file manually.

```
cd /path/to/xtuple
./scripts/import_dictionary.js -d dev -f ../xtuple-linguist/translations/es_MX_dictionary.js
```

Then, from the `UserAccount` workspace of the mobile client, set your locale to `Spanish` (in
this case) and refresh the browser.

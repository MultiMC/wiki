# How to translate

In general, for existing languages, using [crowdin](https://translate.multimc.org) is going to be the best option.

* When there's a technical term that is shared with the operating system (like 'file', 'folder', 'network', 'proxy' and so on), these should use the same terms as the operating system translation.
* When the translations are updated for new source code, the update process guesses when it runs into translations that no longer fit. This creates `fuzzy` translations. It is better to get rid of bad and broken fuzzy translations first.
* A missing translation is better than a wrong/misleading translation.
* Focus on the most exposed strings first. You can use the MultiMC log to determine which translations are used where - it complains about missing and fuzzy translations in `.po` files when they are used.

# Alternate workflow

MultiMC supports hotloading of translations from `GetText Portable Object` (`.po`) files.

The workflow:
* Get a `.po` file from here the [translations repository](https://github.com/MultiMC/MultiMC5-translate).
  * Alternatively, get the `template.pot` and start a new translation based on it.
  * Alternatively, you can also clone the whole repository using `git`.
* Put it in the `translations` folder.
* Edit it with [POEdit](https://poedit.net/) or a similar editor.
* See the changes in real time. MultiMC reloads the translations whenever something changes in the folder.
* When done, post the changed files on [discord](https://discord.gg/multimc), or on [github](https://github.com/MultiMC/MultiMC5-translate) as a pull request.

If you have any questions feel free to hop on [Discord and talk to us](https://discord.gg/multimc).


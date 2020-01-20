# Germinate Translations

Germinate, by default, comes in English. We don't include any other languages into the bundle, because some people may not want the interface to be available in certain languages.

Instead, we offer this repository with all the translations that have been translated by Germinate community members. These are translations of the English template file. This means, that if you changed the English version of any text, you'll have to make corresponding changes to any of the other language files you get from this repository as well.

As an example, let's say you modified `pageDashboardText` to include a custom welcome message in English. You'll then have to modify the same property in the other language files as well.

Currently we offer the following translations:

- German - provided by [Sebastian Raubach](https://github.com/sebastian-raubach)


## Setup

To include these translations in your version of Germinate, please copy them into the `template` subdirectory of the folder provided in your configuration under the property `data.directory.external`.

Then add the locales to the `locales.json` file (or create it if it doesn't exist) in the same directory so that it looks something like this:

```json
[{
  "locale": "en_GB",
  "flag": "gb",
  "name": "British English"
}, {
  "locale": "de_DE",
  "flag": "de",
  "name": "Deutsch - Deutschland"
}]
```

The first entry in this array is the default locale `en_GB`. As an example, `de_DE` has been added. The `name` property can be whatever you want to display on the user interface. `flag` is the [ISO 3166-1 alpha-2](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2) code for the country best representing this locale. `locale` matches the names of the files in this repository (without the file extension).

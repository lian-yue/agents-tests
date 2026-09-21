# agents-tests

A catalog of tests from different models and versions. The home page lists every test and links straight to it.

## About

Each test has two files: a page you can open, and a record with the same name. The record keeps every round: the prompt that was sent, and the agent's reply.

`index.html` is the index. It lists every model, version, date, language, and test. Columns can be sorted, and the list can be filtered.

## Vision

Tests made by different people, models, and versions stay in one place. A later reader can find one test from the index, then see what was asked and what was answered, without searching through a chat.

## Rules

Path:

```
model/version/YYYYMMDD/language/name.unix.html
model/version/YYYYMMDD/language/name.unix.md
```

Example:

```
grok/4.7/20260922/zh/qin-shihuang-assembly.1790011920.html
grok/4.7/20260922/zh/qin-shihuang-assembly.1790011920.md
```

- `model` and `version` are the real names, such as `grok/4.7`.
- The date directory is `YYYYMMDD`, exact to the day, such as `20260922`. Do not use Chinese date words or English month names.
- `language` is the language code of the original prompt and reply, lowercase, such as `zh`, `en`, or `ja`.
- The html file and the md file share the same unix timestamp, so two tests on the same day do not overwrite each other.
- The html file is the page under test.
- The md file states the number of rounds. Every round includes the original prompt and the original agent reply. Do not translate them.
- This README and `index.html` stay in English.
- After adding a test, add that row to the list in `index.html`.

## Pushing

Other people can push.

With write access, push to `main`. Without it, open a pull request.

Include the html file, the md file, and the index update. Follow the path above, and do not replace someone else's unix timestamp.

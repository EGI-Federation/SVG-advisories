# Publishing an advisory

Advisories are to be published by pushing a new file to
[https://github.com/EGI-Federation/SVG-advisories](https://github.com/EGI-Federation/SVG-advisories).

[https://advisories.egi.eu](https://advisories.egi.eu) is built using
[GitHub pages](https://pages.github.com/).

Source files are in
[Markdown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)
format, and [Jekyll](https://jekyllrb.com/) will be used to generate the static
site.

New site builds are triggered automatically whenever the repository is updated.

> It can take up to a few minutes to see the changes being published.

## Overall procedure

> Only selected people having write access to this repository can publish
> advisories.

Advisories are stored in subdirectories named as the current year.

- Use the template `Advisory-SVG-YYYY-XX-Template.md` to create a file in the
  destination directory, renaming using the advisory name (i.e.
  `Advisory-SVG-YYYY-XX.md`)
- Edit the advisory content
- Update the metadata concerning the advisory at the top of the file
  - tile: page title, usually the advisory name `Advisory-SVG-YYYY-XX`
  - published: remove this line or the advisory won't be published, can be
    useful when drafting.
  - permalink: the public to the advisory, allowing to configure the public URL
    used to access the advisory. Only specify what have to be used after
    `https://advisories.egi.eu`
    - permalink `/Advisory-SVG-YYYY-XX` will mean that an advisory stored in the
      `2022` folder will be accessible at this URL:
      `https//advisories.egi.eu/Advisory-SVG-YYYY-XX`
- Edit the relevant index file to reference the new advisory.

### Adding aliases to an advisory

In case an advisory should be reachable by multiple URLs, like for an advisory
covering multiple CVEs, it's possible to specify some URL paths that will be
redirected automatically to the primary URL of the advisory.

This can be achieved by using the `redirect_from` attribute:

```yaml
---
title: Advisory-SVG-CVE-XXXX-XXXX
permalink: /Advisory-SVG-CVE-XXXX-XXXX
redirect_from:
  - /Advisory-SVG-CVE-XXXX-YYYY
  - /Advisory-SVG-XXXXXZZZZ
---
```

This will lead to having the advisory reachable by the following URLs:

- https://advisories.egi.eu/Advisory-SVG-CVE-XXXX-XXXX the permalink and the
  main URL, other links will redirect to this one
- https://advisories.egi.eu/Advisory-SVG-CVE-XXXX-YYYY redirected to
  https://advisories.egi.eu/Advisory-SVG-CVE-XXXX-XXXX
- https://advisories.egi.eu/Advisory-SVG-XXXXXZZZZ redirected to
  https://advisories.egi.eu/Advisory-SVG-CVE-XXXX-XXXX

## Adding content to the repository

> An advisory template is available, see
> [Advisory-SVG-YYYY-XX-Template.md](https://raw.githubusercontent.com/EGI-Federation/SVG-advisories/main/Advisory-SVG-YYYY-XX-Template.md).

It's possible to add files using different ways, by using the GitHub web
interface, using a cloned repository or using an online IDE.

- The standard GitHub web interface is available at:
  [https://github.com/EGI-Federation/SVG-advisories](https://github.com/EGI-Federation/SVG-advisories)
- The GitHub.dev web IDE is available at:
  [https://github.dev/EGI-Federation/SVG-advisories](https://github.dev/EGI-Federation/SVG-advisories)

The standard GitHub web interface is the most simple, but the editor is very
basic.

The GitHub.dev web IDE provides a more advanced editor, and its usage is similar
to what you would do using a local IDE. It's slightly more complex but more
powerful.

> While the next sections documents pushing files directly to the `main` branch,
> it is also possible to make use of
> [Pull Requests](https://docs.github.com/en/pull-requests) so that changes can
> be reviewed and approved before being pushed to production.

### Using the GitHub.com web interface to upload a file created locally

It's possible to prepare the file locally and then upload it to GitHub once it
is ready. Once you have prepared the local file (see the
[advisory template](https://raw.githubusercontent.com/EGI-Federation/SVG-advisories/main/Advisory-SVG-YYYY-XX-Template.md))
that should be named `Advisory-SVG-YYYY-XX.md`, you can upload it by:

- opening
  [https://github.com/EGI-Federation/SVG-advisories](https://github.com/EGI-Federation/SVG-advisories)
- browsing to the destination directory
- Clicking `Add file` -> `Upload files` at the top of the screen
- Selecting the local file
- Adding a `Commit` message
- Clicking `Commit changes`

### Using the GitHub.com web interface to create a file online

Another solution is to edit it online. It can be done in the following way:

- opening
  [https://github.com/EGI-Federation/SVG-advisories](https://github.com/EGI-Federation/SVG-advisories)
- browsing to the destination directory
- Clicking `Add file` -> `Create new file` at the top of the screen
- Naming the file `Advisory-SVG-YYYY-XX.md`
- Adding the file content (see
  [advisory template](https://raw.githubusercontent.com/EGI-Federation/SVG-advisories/main/Advisory-SVG-YYYY-XX-Template.md))
- Adding a `Commit` message
- Clicking `Commit changes`

> If needed edit the relevant index file to reference the new advisory.

Editing the index file can be done in a similar way, by:

- Right clicking the file at
  [https://github.com/EGI-Federation/SVG-advisories](https://github.com/EGI-Federation/SVG-advisories)
- Clicking on the pen icon at the top of the file to edit it
- Adding the reference to the new advisory
- Previewing the change
- Adding a `Commit` message
- Clicking `Commit changes`

### Using the GitHub.dev web IDE to create a file online

Another solution is to edit it online using the
[GitHub.dev web IDE](https://docs.github.com/en/codespaces/the-githubdev-web-based-editor).
It's an IDE based on Microsoft Visual Code.

It can be done in the following way:

- Open
  [https://github.dev/EGI-Federation/SVG-advisories](https://github.dev/EGI-Federation/SVG-advisories)
  (Loading the IDE can take some time, wait for the completion)
- Right click the template file `Advisory-SVG-YYYY-XX-Template.md` => `Copy`
- Right click the destination directory => `Paste`
- Right click the new file create => `Rename`. Name the file
  `Advisory-SVG-YYYY-XX.md`.
- Left click the file to open it, if it's not already opened in a tab.
- Add the file content, it will be automatically saved.
- Once the file is ready you need to commit it to the repository to publish it
- If needed edit the relevant index file to reference the new advisory.
- Open the `Source control` view in the left panel, you should see a GIT icon
  with the number of changed files
- In the `Changes` section, you can review the changes that are to be pushed
- By adding a message in the filed at the top of the changes list, and pressing
  the `Commit and push` button (with a checked icon), you can commit and push
  all the changes at once.
  - If you made multiple changes, it's also possible to select changes to be
    committed, by staging them individually.

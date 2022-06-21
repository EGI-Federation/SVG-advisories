# Publishing an advisory

Repositories are to be published by pushing a new file to
https://github.com/EGI-Federation/SVG-advisories

> Only selected people having write access to this repository can publish
> advisories.

Advisories are stored in subdirectories named as the current year.

- Copy the template `Advisory-SVG-YYYY-XX-Template.md` to the destination
  directory, renaming using the advisory name (i.e. `Advisory-SVG-YYYY-XX.md`)
- Edit the advisory content
- Update the metadata concerning the advisory at the top of the file
  - tile: page title, usually the advisory name `Advisory-SVG-YYYY-XX`
  - published: remove this line or the advisory won't be published, can be
    useful when drafting.
  - permalink: the public to the advisory, allowing to configure the public URL
    used to access the advisory. Only specify what have to be used after
    https://advisories.egi.eu
    - permalink `/Advisory-SVG-YYYY-XX.html` will mean that an advisory stored
      in the `2022` folder will be accessible at those two URLs:
      - `https//advisories.egi.eu/Advisory-SVG-YYYY-XX`
      - `https//advisories.egi.eu/YYYY/Advisory-SVG-YYYY-XX`
- Edit the relevant index file to reference the new advisory.

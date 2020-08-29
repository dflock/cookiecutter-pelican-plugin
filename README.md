# Pelican Plugin CookieCutter Template

This project’s purpose is to make it easy to create new Pelican plugins via a [CookieCutter][] template.

## Requirements

**Option 1**: Install [CookieCutter][] via its [installation instructions](https://cookiecutter.readthedocs.io/en/latest/installation.html).

**Option 2**: Install [Pipx][] and prefix the `cookiecutter` commands below with: `pipx run [...]`

The latter option downloads and runs CookieCutter in a temporary environment. This is useful if you want to occasionally run CookieCutter but don’t need it frequently enough to install it on your computer.

## Usage

To create a new Pelican plugin in the current working directory, enter the following command in your terminal console:

    cookiecutter gh:getpelican/cookiecutter-pelican-plugin

You will then be asked to fill in details about the new plugin. Default values, shown in brackets, can be selected by tapping the `Return` key. While some of these values can be accepted as-is, variables such as the plugin name and authors need to be overridden via the interactive prompts or as arguments to the `cookiecutter` invocation. For example:

    cookiecutter gh:getpelican/cookiecutter-pelican-plugin plugin_name="Render Math" authors='"Jane Smith <jane@example.com>", "Jack Jones <jack@example.com>"'

## Continuous Deployment

The generated plugin contains a `.github/workflows/main.yml` file for continuous integration (CI) and deployment via [GitHub Actions][] and [AutoPub][] that will ensure tests pass, check code style compliance, and publish packaged distributions to PyPI when a `RELEASE.md` file is present. For the latter step to function properly, please first ask a Pelican maintainer to add the necessary tokens to the repository settings.


[CookieCutter]: https://github.com/cookiecutter/cookiecutter
[Pipx]: https://github.com/pipxproject/pipx
[GitHub Actions]: https://github.com/features/actions
[AutoPub]: https://justinmayer.com/projects/autopub/

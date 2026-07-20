# RubyAdminPanel

A framework for creating flexible, powerful admin dashboards in Rails.

![RubyAdminPanel](https://user-images.githubusercontent.com/11917/72203824-ec10f980-3468-11ea-9ac1-51cd28ff88b7.png)

## What's RubyAdminPanel?

RubyAdminPanel is a library for Rails that generates admin dashboards. These give
users clean interfaces that allow them to create, edit, search, and delete
records for any model in the application. RubyAdminPanel aims to provide the best
user experience, and doing as much work as possible for you, whilst also being
flexible to customise.

To accomplish these goals, RubyAdminPanel follows a few guiding principles:

* Stay as close to standard Rails as possible, keeping the
  RubyAdminPanel-specific code as small as practical,
* Support the simplest use cases, and let the user override defaults with
  standard tools such as plain Rails controllers and views,
* Break up the library into core components and plugins, so each component
  stays small and pleasant to maintain.


## How to use

RubyAdminPanel is a [Rails Engine][], but ships with everything needed to
contribute and test new changes.

To maintain compatibility with multiple dependency versions, we use
[Appraisal][].

[Rails Engine]: https://guides.rubyonrails.org/engines.html

### Getting started

1. Fork the repo,
2. Run `./bin/setup` to install the base dependencies and setup a local
   database,
3. Run the test suite: `bundle exec rspec && bundle exec appraisal rspec`,
4. Make your changes,
5. Push your fork and open a pull request.

A good PR will solve the smallest problem it possibly can, have good test
coverage and (where necessary) have internationalisation support.

### Running the application locally

Administrate's demo application can be run like any Rails application:

```sh
bin/dev
```

This will start the application defined in `spec/example_app`.
You can view the `example_app` in the browser by navigating to `/admin`.

## Repository Structure

* The gem's source code lives in the `app` and `lib` subdirectories.
* The demo app is nested within `spec/example_app`.

Rails configuration files have been changed
to recognize the app in the new location,
so running the server or deploying to Heroku works normally.

## Front-end Architecture

This project uses:

* Sass
* [BEM]-style CSS selectors, with [namespaces]
* Autoprefixer
* SCSS-Lint, with [stylelint] ([configuration](stylelint-config))
* A variety of CSS units:
  - `em` for typographical-related elements
  - `rem` for lengths related to components
  - `px` for borders, text shadows, etc.
  - `vw`/`vh` for lengths that should be relational to the viewport

[BEM]: http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
[namespaces]: http://csswizardry.com/2015/03/more-transparent-ui-code-with-namespaces/
[stylelint]: https://stylelint.io

## Icons

We use [Feather][] for icons.

[Feather]: https://feathericons.com

## Labels

Issues and PRs are split into two levels of labels, at the higher level:

* `feature`: new functionality that’s not yet implemented,
* `bug`: breakages in functionality that is implemented,
* `maintenance`: to keep up with changes around us

…and then to more specific themes:

* `namespacing`: models with a namespace,
* `installing`: initial setup, first-run experience, generators,
* `i18n`: translations and language support,
* `views-and-styles`: how administrate looks and is interacted with,
* `dashboards`: how administrate presents fields and displays data,
* `search`: finding things through our models,
* `sorting`: ordering things on dashboards,
* `pagination`: how we handle lots of data in small chunks,
* `security`: controlling data access through authorisation,
* `fields`: new fields, displaying and editing data,
* `models`: models, associations and fetching the underlying data,
* `documentation`: how to use Administrate, examples and common usage,
* `dependencies`: changes or issues relating to a dependency


## Documentation

To customize the appearance, behavior, and contents of the dashboard,
we publish a set docs.

These guides are available as markdown files in the `docs` subdirectory of the
git repository, too.


## Contributing

Please see [CONTRIBUTING.md](/CONTRIBUTING.md).

RubyAdminPanel was originally written by Grace Youngblood and is now maintained by
Nick Charlton. Many improvements and bugfixes were contributed by the [open
source
community](https://github.com/tuoc1226-maker/RubyAdminPanel/graphs/contributors).

## License

RubyAdminPanel is written by Aoto Nakabayashi.

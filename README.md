rspec.github.io
===============

Source for https://rspec.info

Requires a recent version of Ruby (tested on 2.7.5, Ruby 3.x is not yet working), bundler and imagemagick (to generate favicons).

## Local Setup

* `brew install imagemagick` (or your package manager of choice).
* `bundle install`
* `middleman build`

## Local Developing

Run `LIVERELOAD=true middleman server`

## Docker Setup + Development

If you don't have a local Ruby environment suitable to making changes to
rspec.info, or prefer containerised development; use the following scripts to
build the included Docker image and build the site in the containerised
environment instead.

```
# Start the middleman server. Access site at http://localhost:4567
bin/server

# Build the site in the `docs/` directory. Replacement for `middleman build`.
bin/build

# Start a console inside the docker container. Useful for debugging or running commands locally.
bin/console
```

## Deploying

Run `bundle exec middleman build`, which will compile the site to `./docs`. This folder is directly
served from the `source` branch via the config settings for github pages so in order to deploy you
only need to run the command locally and push up a PR to your target of choice, which are:

- To update [https://rspec-staging.gihub.io](https://rspec-staging.gihub.io) use repository https://github.com/RSpec-Staging/rspec-staging.github.io/.
- To update [https://rspec.info](https://rspec.info) use repository https://github.com/rspec/rspec.github.io/

## Credits

[Andrew Harvey](https://mootpointer.com) - for his incredible effort of making this repository as it is now

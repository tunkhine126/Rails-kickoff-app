# README

Work in progress for creating an application template.

# INCLUDED GEMS
devise
friendly_id
sidekiq
name_of_person
stripe
rspec
factorybot
css-bundling
tailwind css

# USAGE
When creating a new rails app simply pass the template filename and ruby extension through. I opt for esbuild instead of the default importmap configuration for JavaScript.

```bash
$ rails new sample_app -j esbuild -m kickoff_app/template.rb
```

# Once installed what do I get?

- [Tailwind CSS](https://tailwind.com)
- [Devise](https://github.com/plataformatec/devise) with a new `name` field already migrated in. The name field maps to the `first_name` and `last_name` fields in the database thanks to the [`name_of_person`](https://github.com/basecamp/name_of_person) gem.
- Enhanced views and devise views using Tailwind CSS.
- The [Stripe](https://rubygems.org/gems/stripe/) gem installed with the Stripe API to make accepting payments on the web. Be sure to add your own unique API keys.
- Support for Friendly IDs thanks to the handy [friendly_id](https://github.com/norman/friendly_id) gem. Note that you'll still need to do some work inside your models for this to work. This template installs the gem and runs the associated generator.
- [Rspec-rails](https://github.com/rspec/rspec-rails) testing framework for rails.
- [Factorybot](https://github.com/thoughtbot/factory_bot_rails) a fixtures replacement with a straightforward definition syntax, support for multiple build strategies, and support for multiple factories for the same class, including factory inheritance.
- Optional Foreman support. Run `.bin/dev` to kick off rails and Tailwind processes. Foreman needs to be installed as a global gem on your system for this to work. i.e. `gem install foreman`
- Custom view helper defaults for basic button and form elements.
- Scaffolding templates made with Tailwind CSS

### Boot it up

`$ ./bin/dev` 
# 0.2.0

## API Changes

* `Controller#present` no longer calls `respond_to`, but lets you do the rendering. This will soon be re-introduced using `respond(present: true)`.
* `Controller#form` did not respect builders, this is fixed now.
* Use `request.body.read` in Unicorn/etc. environments in `Controller#respond`.

## Stuff

* Autoloading changed, again. We now `require_dependency` in every request in dev.

# 0.1.3

* `crud_autoloading` now simply `require_dependency`s model files, then does the same for the CRUD operation file. This should fix random undefined constant problems in development.
* `Controller#form` did not use builders. This is fixed now.

# 0.1.2

* Add `crud_autoloading`.

# 0.1.1

* Use reform-1.2.0.

# 0.1.0

* First stable release after almost 6 months of blood, sweat and tears. I know, this is a ridiculously brief codebase but it was a hell of a job to structure everything the way it is now. Enjoy!
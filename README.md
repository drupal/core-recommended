# drupal/core-recommended-dependencies

This project is for use with a Composer-managed Drupal site. It is recommended
that all Composer-managed Drupal sites use this project.

Require this project *instead of* the [drupal/core](https://github.com/drupal/core)
subtree split in order to guarentee that all of the dependencies from
`drupal/core` will be included in your Drupal site at exactly the same version
that was tested with the version of Drupal you are currently using.

The consequences of *not* using this project is that Drupal's dependencies
may "float up" to more recent versions than were tested with Drupal when you
use Composer to upgrade your Drupal site. Occasionally, new dependency versions
introduce bugs in Drupal. While these sorts of errors are usually corrected
fairly quickly, it can still be quite disruptive to be one of the first people
encountering one of these bugs. Using the recommended dependencies avoids this
problem by only using dependency versions that have already been tested with
Drupal.

## Upgrading

When using this project, upgrade your Drupal site as follows:
```
$ composer update drupal/core-recommended-dependencies --with-dependencies
```
This will update `drupal/core` and any needed dependencies.

Running a simple `composer update` will also update `drupal/core`, all of
Drupal's dependencies (to the correct tested versions), and all of your
contrib modules and other dependencies.

## References

This project is derived from the original community project
[webflo/drupal-core-strict](https://github.com/webflo/drupal-core-strict).
It was generated from tools derived from [webflo/package-generator-drupal](https://github.com/webflo/package-generator-drupal)
and [webflo/package-generator](https://github.com/webflo/package-generator).

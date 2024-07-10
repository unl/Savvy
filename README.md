# Savvy

Savvy is a powerful but lightweight object-oriented template system for PHP.

Unlike other template systems, Savvy by default does not compile your
templates into PHP; instead, it uses PHP itself as its template language so you
don't need to learn a new markup system.

## Note for php 8.1

For php 8.1 we swapped using Saltybeagle's package to this repo. We did this so we can more easily update and maintain the package.

### Update to composer.json

```JSON
{
    "type":"package",
    "package": {
        "name": "unl/savvy",
        "version": "master",
        "source": {
            "url": "https://github.com/unl/Savvy.git",
            "type": "git",
            "reference": "master"
        }
    }
}
```

1. First we added the repo to the "repositories" section in the json file
2. We then changed `"saltybeagle/savvy": "#.#",` to `"unl/savvy": "dev-master",` so we always pull from the master branch
3. We also need to add `"Savvy": "vendor/unl/savvy/src"` in the psr-0 section of the the autoload so that Savvy's namespace is used correctly
4. After all the changes are made we may need to clear the cache and re-install `composer clear-cache && composer install`

[Saltybeagle's Package](https://packagist.org/packages/saltybeagle/savvy)

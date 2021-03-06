## Composer Package Generator

This very simple PHP script will generate the following structure, ready to start 
creating your composer package.

     ┐
     ├── src
     ├── tests
     │   ├── fixtures
     │   ├── VendorPackageTest.php (generated based upon your namespace)
     │   └── bootstrap.php
     ├── .gitignore
     ├── .scrutinizer.yml
     ├── .styleci.yml
     ├── .travis.yml
     ├── CONTRIBUTING.md
     ├── LICENSE
     ├── phpunit.xml
     ├── README.md
     └── composer.json
     

## Install

Git clone this project:

``` bash
$ git clone git@github.com:lcherone/composer-package-generator.git .
```

Don't forget to delete the `.git/` folder!


## Generate your project files, like a boss!

Open up and edit `setup.php`, enter your details in the following array:

    /**
     * Define the package settings
     */
    $package = [
        'name' => 'vendor/package',
        'title' => 'My Package',
        'description' => 'This is my package, description.',
        'type' => 'library',
        'keywords' => [
            'example', 'project', 'boilerplate', 'package'
        ],
        'homepage' => 'http://github.com/vendor/package',
        'authors' => [
            [
                'name' => 'Your Name',
                'email' => 'your-email@example.com',
                'homepage' => 'http://github.com/vendor',
                'role' => 'Owner'
            ]
        ],
        'autoload' => [
            'psr-4' => [
                'Vendor\\Package\\' => 'src',
            ]
        ],
        'autoload-dev' => [
            'psr-4' => [
                'Vendor\\Package\\Tests\\' => 'tests',
            ]
        ]
    ];

Once you edited the array, save the file and then run the following to generate 
your project files:

``` bash
$ php setup.php
```

Examine the generated files and make your tweeks, especially the `README.md` which 
your need to finish off. 

**Badges:**

Markdown links and images will have been added to the `README.md` and should work 
once you push your project and enable the project on these 3rd party sites.

 - [`Build Status (https://travis-ci.org)`](https://travis-ci.org)
 - [`StyleCI (https://styleci.io)`](https://styleci.io)
 - [`Scrutinizer (https://scrutinizer-ci.com)`](https://scrutinizer-ci.com)
 - [`Packagist (https://packagist.org)`](https://packagist.org/)
<!-- end list -->

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.


## Credits

 - [Lawrence Cherone](http://github.com/lcherone)
 - [All Contributors](../../contributors)


## License

The MIT License (MIT). Please see [License File](LICENSE) for more information.

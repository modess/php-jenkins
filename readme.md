# laravel-jenkins

Boilerplate for setting up continuous integration of [Laravel 4](http://www.laravel.com/) using [Jenkins](http://www.jenkins-ci.org)

We did not want to delete and recreate the vendor folder everytime that the script was ran, so "composer update" is ran if the vendor folder exist--otherwise "composer install" is ran.  In order to force a clean vendor folder, you can run one of the builds with the "-clean"…

	ant build-clean
	OR
	ant build-parallel-clean


### Build Targets
Here are the list of build targets that are defined within the build.xml:

* build *(DEFAULT)*
* build-clean
* build-parallel
* build-parallel-clean
* build-common
* tools-parallel - Run tools in parallel
* clean - Cleanup build and composer artifacts
* clean-build - Cleanup build artifacts
* clean-composer - Cleanup composer artifacts
* composer - Install or update dependencies
* composer.check
* composer-install - Installing dependencies
* composer-update - Updating dependencies
* lint - Perform syntax check of sourcecode files
* pdepend - Calculate software metrics using PHP_Depend
* phpcb - Aggregate tool output with PHP_CodeBrowser
* phpcpd - Find duplicate code using PHPCPD
* phpcs - Find coding standard violations using PHP_CodeSniffer and print human readable output. Intended for usage on the command line before committing
* phpcs-ci - Find coding standard violations using PHP_CodeSniffer creating a log file for the continuous integration server
* phpdox - Generate API documentation using phpDox
* phploc - Measure project size using PHPLOC
* phpmd - Perform project mess detection using PHPMD and print human readable output. Intended for usage on the command line before committing.
* phpmd-ci - Perform project mess detection using PHPMD creating a log file for the continuous integration server
* phpunit - Run unit tests with PHPUnit
* prepare - Prepare for build
* storage-permissions - Setting storage permissions
* storage-permissions.unix - Setting storage permissions on unix
* storage-permissions.windows - Setting storage permissions on windows
* storage.unix.check - Check for app/storage on unix
* storage.windows.check - Check for app/storage on windows

### References
This boilerplate comes from glueing together a collection of post on the internet
* [https://modess.io/continuous-integration-for-laravel-with-jenkins-and-git/](https://modess.io/continuous-integration-for-laravel-with-jenkins-and-git/)
* [http://chris.schalenborgh.be/2013/04/05/deploy-php-projects-jenkins-os/](http://chris.schalenborgh.be/2013/04/05/deploy-php-projects-jenkins-os/)

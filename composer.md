Override PHP base dependency in composer

This package requires php ^7.3 but your PHP version (7.2.34) does not satisfy that requirement.

composer install --ignore-platform-reqs



composer update

php -d memory_limit=-1 `which composer` update

composer self-update --preview

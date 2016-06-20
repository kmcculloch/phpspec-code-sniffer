# phpspec-code-sniffer

Very simple PHPSpec code sniffing, based on PSR1 and PSR2

Kevin McCulloch <p.kevin.mcculloch@gmail.com>

## Purpose

I wrote this module so that I could easily toggle a phpcs standard that won't
throw errors for PHPSpec's non-camel-case it_does_something() function naming
convention. All it does is apply PSR1 and PSR2 while ignoring the camel-case
function naming rule. Stupidly simple, really. I'd be open to expanding the
ruleset if others find this useful.

## Global Installation

If you have phpcs installed globally (which generally involves running
`composer global require squizlabs/php_codesniffer:~2.0` and adding `~/.composer/vendor/bin` to your `$PATH`), you can add this ruleset like so:

```
composer global require kmcculloch/phpspec-code-sniffer:1.x-dev

# Tell phpcs where to find the ruleset:
phpcs --config-set installed_paths ~/.composer/vendor/kmcculloch/phpspec-code-sniffer/

# Run the following and confirm that you can see "PHPSpec" in the list of
# installed standards:
phpcs -i

# Sniff your code:
phpcs --standard=PHPSpec ~/path/to/MyClassSpec.php
```

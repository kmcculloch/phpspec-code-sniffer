# phpspec-code-sniffer

Very simple PHPSpec code sniffing, based on PSR1 and PSR2

## Purpose

I wrote this module so that I could easily toggle a phpcs standard that won't
throw errors for PHPSpec's non-camel-case it_does_something() function naming
convention. All it does is apply PSR1 and PSR2 while ignoring the camel-case
function naming rule.

## Installation

composer global config repositories.phpspec-code-sniffer vcs https://github.com/kmcculloch/phpspec-code-sniffer

composer global require kmcculloch/phpspec-code-sniffer


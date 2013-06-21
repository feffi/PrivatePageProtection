### Disclaimer
This is a fork of the original Mediawiki extension <a href="http://www.mediawiki.org/wiki/Extension:PrivatePageProtection">PrivatePageProtection</a> by Daniel Kinzler (<a href="http://www.mediawiki.org/wiki/User:Duesentrieb">Duesentrieb</a>)
___

### Description
The *PrivatePageProtection* extension implements a way to restrict access to specific pages using a parser function. Using that parser function, the user groups that should have access to the page can be listed directly in the page.
___

### Installation
First of all clone this repository to an existing git project

```bash
git clone https://github.com/feffi/PrivatePageProtection.git
```

or clone this repository to an existing git project

```bash
git submodule add https://github.com/feffi/PrivatePageProtection.git extensions/PrivatePageProtection
```

Secondly add the required files to your `LocalSettings.php`:
```php
require_once("$IP/extensions/PrivatePageProtection/PrivatePageProtection.php");
```
___
### Usage
To restrict access to a page, use the `allow-groups` function:

```{{#allow-groups:sysop}}```

would restrict access to the `sysop` group.

```{{#allow-groups:autoconfirmed|emailconfirmed}}```

restricts access to members of the `autoconfirmed` and `emailconfirmed` groups.
> Note that user can not save a page which restricts access to groups the user does not belong to. That is, users can not lock themselves out of pages.

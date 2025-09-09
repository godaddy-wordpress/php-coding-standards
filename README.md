# SkyVerge PHP Coding Standards

This is the PHP Codesniffer ruleset that contains the PHP coding standards for SkyVerge.

## Rulesets

- **SkyVerge_PHP_Base** - Legacy SkyVerge coding style rules (mostly deprecated).
- **SkyVerge_Woo_Functions** - Defines custom WooCommerce and SkyVerge escaping and sanitization functions.
- **WooCommerce_Marketplace_Security** - Security configuration used by WooCommerce Marketplace QIT security scans.
- **SkyVerge_Woo_Security** - Combines WooCommerce security scanning with SkyVerge custom functions. This is the recommended ruleset for SkyVerge PHPCS workflows and configurations.

## Sample config file

```xml
<?xml version="1.0"?>
<ruleset name="SkyVerge WooCommerce Plugin">
	<description>SkyVerge Plugin Codesniffer configuration</description>

	<file>.</file>

	<exclude-pattern>*/i18n/*</exclude-pattern>
	<exclude-pattern>*/lib/*</exclude-pattern>
	<exclude-pattern>*/vendor/*</exclude-pattern>
	<exclude-pattern>*/node_modules/*</exclude-pattern>
	<exclude-pattern>*/build/*</exclude-pattern>
	<exclude-pattern>*/tests/*</exclude-pattern>

	<rule ref="SkyVerge_Woo_Security" />

</ruleset>
```
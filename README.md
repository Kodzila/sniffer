# Sniffer

This is a library containing shared PHP CodeSniffer configuration.

Then install via composer:
```bash
composer require kodzila/sniffer --dev
```

## Configuration
In the root project create a file `phpcs.xml` with configuration:
```bash
<?xml version="1.0"?>
<ruleset>
    <description>App project</description>

    <rule ref="./vendor/kodzila/sniffer/ruleset.xml"/>
</ruleset>
```


You can also specify Sniff paths:
```bash
<?xml version="1.0"?>
<ruleset>
    <description>App project</description>

    <rule ref="./vendor/kodzila/sniffer/ruleset.xml"/>

    <file>src/</file>
    <exclude-pattern>src/Migrations/*</exclude-pattern>
    <exclude-pattern>src/Kernel.php</exclude-pattern>
</ruleset>
```

## Rules documentation
* [Base codesniffer](https://github.com/squizlabs/PHP_CodeSniffer/wiki/Customisable-Sniff-Properties)
* [Slevomat](https://github.com/slevomat/coding-standard)
* [Custom ruleset](https://github.com/doctrine/coding-standard/blob/master/lib/Doctrine/ruleset.xml)

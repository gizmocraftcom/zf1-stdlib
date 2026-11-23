# Changelog

## 2.0.0

Fork of `diablomedia/zendframework1-stdlib`, published as `gizmocraft/zendframework1-stdlib`.

### Breaking changes

- Requires PHP `>=8.5`. Tested on PHP 8.5 and 8.6.
- Package renamed from `diablomedia/zendframework1-stdlib` to `gizmocraft/zendframework1-stdlib`.
- No public API changes. The only library change is `Zend_Stdlib_SplPriorityQueue` referencing `SplPriorityQueue::EXTR_BOTH` and `SplPriorityQueue::EXTR_DATA` instead of `self::`, which behaves the same and satisfies PHPStan.

### Other changes

- Dev dependencies upgraded (PHPUnit 13, PHPStan 2.3, php-cs-fixer 3.95, GrumPHP 2.27). Dropped `composer-require-checker`, which has no release for PHP 8.6.
- Tests migrated to PHPUnit 13 attributes. CI runs PHP 8.5 and 8.6.
- PHPStan ignore patterns updated for the current PHPStan messages; the obsolete `$key` ignore was removed.

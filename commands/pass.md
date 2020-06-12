# Pass

[source](https://www.passwordstore.org)

## show passwords too

```bash
pass Email/zx2c4.com
# sup3rh4x3rizmynam3
```

## copy them to the clipboard

```bash
pass -c Email/zx2c4.com
# Copied Email/jason@zx2c4.com to clipboard. Will clear in 45 seconds.
```

## We can add existing passwords to the store with insert

```bash
pass insert Business/cheese-whiz-factory
# Enter password for Business/cheese-whiz-factory: omg so much cheese what am i gonna do
```

> This also handles multiline passwords or other data with --multiline or -m, and passwords can be edited in your default text editor using pass edit pass-name.

## The utility can generate new passwords using /dev/urandom internally

```bash
pass generate Email/jasondonenfeld.com 15
# The generated password to Email/jasondonenfeld.com is:
# $(-QF&Q=IN2nFBx
```

> It's possible to generate passwords with no symbols using --no-symbols or -n, and we can copy it to the clipboard instead of displaying it at the console using --clip or -c.

## Remove

```php
pass rm Business/cheese-whiz-factory
# rm: remove regular file ‘/home/zx2c4/.password-store/Business/cheese-whiz-factory.gpg’? y
# removed ‘/home/zx2c4/.password-store/Business/cheese-whiz-factory.gpg’
```

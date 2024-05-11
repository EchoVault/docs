---
sidebar_position: 1
---

# SET

Syntax:

```
SET key value [NX | XX] [GET] [EX seconds | PX milliseconds |
EXAT unix-time-seconds | PXAT unix-time-milliseconds]
```

Module: `generic`

ACL Categories: `@write`, `@slow`

Set the value of a key, considering the value's type. If the key already exists, it is overwritten.

Options:

- NX - Only set if the key does not exist.
- XX - Only set if the key exists.
- GET - Return the old value stored at key, or nil if the value does not exist.
- EX - Expire the key after the specified number of seconds (positive integer).
- PX - Expire the key after the specified number of milliseconds (positive integer).
- EXAT - Expire at the exact time in unix seconds (positive integer).
- PXAT - Expire at the exat time in unix milliseconds (positive integer).
---
layout: page
permalink: /docs/commands.html
title: Mongrate CLI commands
content_title: Commands
---

### Generate migration

To generate a migration file, with the name "UpdateAddressStructure":

```
mongrate generate-migration UpdateAddressStructure
```

The current date will automatically be appended to the migration name, to help prevent duplicate
names and conflicts.

### List migrations

To list available migrations:

```
mongrate list-migrations
```

### Toggle migration

To toggle a migration between down and up (useful while writing your migration's tests):

```
mongrate toggle UpdateAddressStructure_20140523
```

### Migrate up

To migrate one migration up:

```
mongrate up UpdateAddressStructure_20140523 [--force]
```

To migrate all unapplied migrations up:

```
mongrate up-all
```

### Migrate down

To migrate down:

```
mongrate down UpdateAddressStructure_20140523 [--force]
```

### Test migration

To verify a migration with it's YML test files:

```
mongrate test UpdateAddressStructure_20140523 (up|down|empty) [--pretty]
```

If you leave the direction empty, it will test both going `up` and `down`.

If you add `--pretty=1`, the output of any errors will be formatted nicely, which is easier to read,
but uses more vertical screen area.

To test all migrations:

```
mongrate test-all
```

### Update Mongrate

To update the Mongrate executable:

```
mongrate self-update
```

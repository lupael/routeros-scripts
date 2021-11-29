Send backup via e-mail
======================

[◀ Go back to main README](../README.md)

🛈 This script can not be used on its own but requires the base installation.
See [main README](../README.md) for details.

Description
-----------

This script sends binary backup (`/ system backup save`) and complete
configuration export (`/ export terse`) via e-mail.


Requirements and installation
-----------------------------

Just install the script:

    $ScriptInstallUpdate email-backup;

Configuration
-------------

The configuration goes to `global-config-overlay`, these are the parameters:

* `BackupSendBinary`: whether to send binary backup
* `BackupSendExport`: whether to send configuration export
* `BackupPassword`: password to encrypt the backup with
* `BackupRandomDelay`: delay up to amount of seconds when run from scheduler

Also valid e-mail settings are required to send mails.

Usage and invocation
--------------------

Just run the script:

    / system script run email-backup;

Creating a scheduler may be an option:

    / system scheduler add interval=1w name=email-backup on-event="/ system script run email-backup;" start-time=09:15:00;

See also
--------

* [Upload backup to Mikrotik cloud](cloud-backup.md)
* [Upload backup to server](upload-backup.md)

---
[◀ Go back to main README](../README.md)  
[▲ Go back to top](#top)

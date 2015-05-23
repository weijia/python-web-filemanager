# Database Export #
Export file need to met the following requirements:
  * Import a backup twice will not impact the data in database
    * Backup file will contain an id, if it has been imported
  * If an item was imported twice, only 1 instance will exists.
    * Every item should have a global ID
      * Use timestamp, key, value, user, dbName, machine ID?
  * No info loss?

# export file format #
  * {"backup-uuid":"xxxxx-xxxx-xxxxx-xxxxx-xxxx",
  * "time-duration":"first records' timestamp, last records' timestamp"
  * "add":
    * [{"ta": timestampWhenAdding, "key": key, "value": value, "dbName": dbName, "user", user, "exporter": exporter, "valid": True},],
  * "remove":
    * ["ta": timestampWhenAdding, "tm": timestampWhenRemoving, "key": key, "value": value, "dbName": dbName, "user", user, "valid": False],
  * }

  1. timestampWhenExporting is used to identify if this item is imported or is added locally. imported item will

Add your content here.  Format your content with:
  * Text in **bold** or _italic_
  * Headings, paragraphs, and lists
  * Automatic links to other wiki pages
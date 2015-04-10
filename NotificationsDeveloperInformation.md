# Introduction #

The only accepted characters are Alpha, Numeric and the following: < > - 

Notifications will accept HTML tags like `<br>`

Once you send information to either of the below scripts, a notification will be created in the user specified Notifications path.


# Details #

## PHP: ##

The PHP script resides at: /plugins/Notifications/notify.php

The following POST strings are accepted, all must be sent for notification to be made:

  * cmd: "add"
  * plugin: "Plugin Name"
  * subject: "Notification Subject"
  * description: "Notification description"
  * importance: "default,warning or alert"

Example jQuery code:

```
$.post("/plugins/Notifications/notify.php", { cmd: "add", plugin: "Plugin Name", subject: "Notification Subject", description: "Notification description", importance: "default,warning or alert"});
```



## BASH Script: ##

See example below. Call on the bash script, add variables inside quotation marks. All fields are required in this specific order:

```
/usr/local/emhttp/plugins/Notifications/notify.sh -plugin "Plugin Name" -subject "Notification Subject" -description "Notification description" -importance "default,warning or alert"
```
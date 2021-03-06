# Advanced Configuration

MailerQ can be configured using the "/etc/mailerq/config.txt" config file. 
Most of the variables and settings in this config file are discussed in 
seperate articles. However, the following settings are not mentioned
anywhere else:

````
max-delivertime:        86400
max-attempts:           0
server-id:              1
license:                /path/to/license.txt
user:                   username
lock:                   /path/to/lock.txt
````

Most of the settings speak for themselves. A small overview.


## Max deliver time

When a mail gets greylisted, or when there is an other type of soft failure, 
MailerQ reschedules the mail for later delivery. Inside the JSON data
of each message you can add the optional properties "maxdelivertime" and 
"maxattempts" that instruct MailerQ how long it should retry to deliver
the message, and when it should give up trying.

If you do not include these properties, MailerQ falls back to the 
"max-delivertime" and "max-attempts" config file settings. The 
"max-delivertime" variable holds the number of seconds it should try,
and "max-attempts" the total number of attempts before giving up.

You should normally set the "max-attempts" value to 0, meaning unlimited.
MailerQ will then only give up after a certain amount of time, no matter
how many attempts are made. In practice, the interval between attempts get
longer after the number attempts. The first retry is only a couple of 
minutes after the initial attempts, but later attempts follow after longer
intervals.


## Server ID

Each message that is accepted by MailerQ gets a unique message ID. To
prevent that two running MailerQ instances both assign exactly the same
ID to a message, you can assign a "server-id" variable. This identifier
guarantees that message ID's will never conflict.

````
server-id:      1
````

## License

To work properly, MailerQ needs a license file. The license file can be 
[downloaded](http://mailerq.com/product/license "MailerQ license") from the 
MailerQ website. You can store the file anywhere on the file system. The path to 
the license file can be configured by setting 

````
license:        <Path to your license> (empty by default)
````

## User

If you have configured MailerQ to use ports lower than 1024 (like port 25 for 
SMTP and/or port 80 for the management console), the MTA must be started as user 
"root". Once the ports have been opened, MailerQ changes its identity to the user 
set in the config file.

````
user:           <user name> (empty by default)
````

The user name to change identify to after the SMTP and HTTP ports have been opened.


## Lockfile

To prevent that MailerQ starts more than once, MailerQ stores its process ID 
(pid) in a lockfile. The name and location of the lockfile can be set in the 
configuration file.

````
lock: <filename>            (default: /tmp/mailerq.pid)
````

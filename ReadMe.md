# Reminders Command Line Tool #

Command line tool for OS X’s Reminders application

## usage ##

```
reminders [listname] [help|open|show] [add|check|uncheck|delete reminder]
```

## commands ##

### listing items###

` reminders `: lists the items in “unsorted”

`reminders listname`: list the items in the list named `listname`

`reminders show` or `reminders open`: open the “unsorted” list in the Reminders application

`reminders listname show`: show the list named `listname` in the Reminders application

### list output ###
The result of a reminders command will look like this:

```
> reminders 'CLI Tool'
Reminders: CLI Tool
 √ uncheck an item
 √ add an item
 √ check an item
 √ delete an item
   - upload to github
```

The first line is show the name of the list, area or project the command was working on.

Then the tool will list the items. Completed items have a `√` and open (not completed) items have a `-`. Checked items that have been completed more than two days ago will not be shown. Reminders that have their due date in the future will also not be shown.


### adding items ###

` reminders add do this soon`: adds a new reminder named `do this soon` to the “unsorted” list

`reminders listname add do this soon, too`: adds a new reminder named `do this soon, too` to the list named `listname`

### checking items ###

`reminders check someitem`: checks the first reminder in the “unsorted” list whose name starts with `someitem`

`reminders uncheck someitem`: unchecks the first reminder in the "Today" list whose name starts with `someitem`

`reminders cancel someitem`: cancels the first reminder in the “unsorted” list whose name starts with `someitem`

`reminders listname check someitem`: checks the first reminder in the list, area or project named `listname` whose name starts with `someitem`

`reminders listname uncheck someitem`: unchecks the first reminder in the list `listname` whose name starts with `someitem`

`reminders listname delete someitem`: deletes the first reminder in the list named `listname` whose name starts with `someitem`

###other commands###

`reminders help`: shows usage

## installation##
The `reminders` script will be happy anywhere in your `$PATH`, or alternatively you can clone the project and put a symlink to the script in `/usr/local/bin` or elsewhere in your `$PATH`.


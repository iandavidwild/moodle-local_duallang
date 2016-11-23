# Example of custom string manager for Moodle

This is an example of the implementation of a custom string manager for Moodle 2.9 and higher.

It is not supposed to be actually used. It should serve as an illustration or a base point for your own development. This plugin was
primarily written to test the support for custom string managers in the Moodle core.

## Installation

1. Install this plugin

        $ cd /path/to/your/moodle/dirroot
        $ cd local
        $ git clone https://github.com/mudrd8mz/moodle-local_stringman.git stringman

2. Edit your main `config.php` and add the following line there. Of course, you have to add this line before the `setup.php` is
   included at the end of the file.

        $CFG->customstringmanager = '\local_stringman\dummy_string_manager';

3. Check that all texts normally displayed by `get_string()` are now replaced with some dummy information like `{login//core}`.

## More documentation

See https://tracker.moodle.org/browse/MDL-49361 for more details and reasoning behind this feature.

Main Configuration
==================

The main configuration for Total Economy is ``totaleconomy.conf``. From this file, you can enable/disable features, modify currency and database settings, set the language, and other general settings.

Enabling/Disabling Features
---------------------------
Total Economy's features can be enabled/disabled to best suit the needs of your server. These features can easily be disabled by setting its value to false, or enabled by setting its value to true.

Some features have extra settings to better fine tune them to your needs.

Currency Settings
-----------------
Total Economy supports multiple currencies and are effortless to setup. To create your own, simply copy and paste the default ``dollar`` currency and change the values to match your currency.
::

    coin {
        // Plural form of the currency name
        currency-plural=Coins

        // Singluar form of the currency name
        currency-singular=Coin

        // Whether this should be the default currency
        default=false

        // Display the symbol to the left (true)
        // or right (false) of the balance
        prefix-symbol=true

        // Starting balance for new players
        startbalance="100"

        // Symbol displayed next to the balance
        symbol="$"

        // Can this currency be transfered (/pay)
        // to other players
        transferable=true
    }

Save Interval
-------------

Total Economy saves the account configuration file every 30 seconds by default instead of saving changes immediately. To disable this and go back to saving the account configuration file as soon as changes are made, the value stored in save-interval can be set to 0.

If you're using a database, this setting can be ignored.

Database Settings
-----------------

By default, database support is disabled and all account data will be stored within the accounts configuration file. Database settings can be found within the database block:
::

    database {
        // Enable/Disable database support
        enable=false

        // Database username
        user=""

        // Database password
        password=""

        // The URL of the database
        url="mysql://[URL]:[PORT]/[DATABASE]"
    }

**Be sure the create the database before starting the server**

Language
--------

TotalEconomy has support for a few different languages thanks to translations provided by the wonderful community. For a list of supported languages check out this directory_.

Within that directory are a few ``messages_*.conf`` files. The  combination of characters after ``messages_`` and before ``.conf`` is the language. Changing the language is as simple as swapping the default ``en`` with one of the other available languages.

.. _directory : https://github.com/Erigitic/TotalEconomy/tree/develop/src/main/resources/assets/totaleconomy

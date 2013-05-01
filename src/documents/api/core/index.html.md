---
title: Superstartup API
layout: docs
---

Methods and properties available.

## Methods

### ss and ss.init

The method `ss.init` will kick off the Superstartup library, initializing all attached components. A promise is returned or a callback is accepted. `ss` is an alias of `ss.init`.

    ss( [callback] )
    ss.init( [callback] )


### ss.isReady

Returns boolean, whether the Superstartup library has been initialized.

    if ( ss.isReady() ) { /* ... */ }

### ss.listen

Attach listeners to events emitted by Superstartup.

    ss.listen( eventType, callback [, selfObject] )

**Returns** A unique identifier, use it to remove the listener with `ss.unlisten`.

Read the full documentation on the [Superstartup Events][events] page.

### ss.unlisten

Remove a listener added using `ss.listen`.

    ss.unlisten( listenerId )

Read the full documentation on the [Superstartup Events][events] page.

### Method `ss.config()`

Configure Superstartup. This method allows for both setting and getting config values, depending on the argument count and type.

    ss.config( key [, value] )

Possible uses of `ss.config`:

* `key` is string, no `value` defined, will return the configuration value of that key.
* `key` is an Object with key/value pairs, will set the values for all the provided keys.
* `key` is string and a `value` is provided, will set that key with the provided value.

Read the full documentation on the [Superstartup Config][config] page.



[events]: /api/events/ "Superstartup Events"
[config]: /api/config/ "Superstartup Configuration"

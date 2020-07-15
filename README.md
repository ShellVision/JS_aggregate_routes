# JS_aggregate_routes
JavaScript Code that takes a list of prefixes and :
*  Remove any supplied prefixes which are superfluous because they are already included in another supplied prefix. For example, 10.0.2.0/24 would be removed if 10.0.0.0/17 was also supplied.
*  Identifies adjacent prefixes that can be combined under a single, shorter-length prefix. For example, 10.0.2.0/24 and 10.0.3.0/24 can be combined into the single prefix 10.0.2.0/23



For example in the INPUT if we have
* 10.0.0.0/19
* 10.0.255.0/24
* 10.1.0.0/24
* 10.1.1.0/24
* 10.1.2.0/24
* 10.1.2.0/25
* 10.1.2.128/25
* 10.1.3.0/25

The OUTPUT should be
* 10.0.0.0/19
* 10.0.255.0/24
* 10.1.0.0/23
* 10.1.2.0/24
* 10.1.3.0/25

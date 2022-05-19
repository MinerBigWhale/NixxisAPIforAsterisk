# NixxisAPIforAsterisk
A web api that allows the asterisk to easily query rest api

## Introduction
Asterisk as multiple way to interract with rest API but many are not easy to handle and implement.
I wanted an easy way to query data and especialy an easy way to parse response.

The easyest way for me is to have a string of keys and values encoded in key-value pairs separated by '&', with a '=' between the key and the value.
like so key1=value1&key2=value2&key3=value3

this can be easily parse using split functions and loops.

## API middleware
The middleware have the objective of querying services and format the response for aserisk.
I choose Asp.net cause we already had a Windows server on hand.
The server provide a swagger for the api definition and is organized around controllers exposed to the Asterisk with an output formater that transform json into string of key-value pairs and servicies to query various apis.
Nixxis Api is an included service and a template for basic, bearer and api-key header are included.

## Asterisk dialplan
the query and parser are defined here for ease of use.


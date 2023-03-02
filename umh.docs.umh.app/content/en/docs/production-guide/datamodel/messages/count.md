+++
title = "count"
description = "Count Messages are sent everytime an asset has counted a new item."
+++

## Topic

MQTT: ``ia/<customerID>/<location>/<AssetID>/count``

{{% notice note %}}
For Kafka just switch the `/` character with a `.`
{{% /notice %}}

## Usage

A count message is send everytime an asset has counted a new item.

## Content

| key            | data type | description                                                 |
|----------------|-----------|-------------------------------------------------------------|
| `timestamp_ms` | `int64`   | unix timestamp of message creation                          |
| `count`        | `int64`   | amount of items counted                                     |
| `scrap`        | `int64`   | *optional* amount of defective items. In unset 0 is assumed |


### JSON

#### Examples

One item was counted and there was no scrap:
```json
{
  "timestamp_ms":1589788888888,
  "count":1,
  "scrap":0
}
```

Ten items where counted and there was five scrap:
```json
{
  "timestamp_ms":1589788888888,
  "count":10,
  "scrap":5
}
```

#### Schema

```json
{
    "$schema": "http://json-schema.org/draft/2019-09/schema",
    "$id": "https://learn.umh.app/content/docs/datamodel/messages/count.json",
    "type": "object",
    "default": {},
    "title": "Root Schema",
    "required": [
        "timestamp_ms",
        "count"
    ],
    "properties": {
        "timestamp_ms": {
            "type": "integer",
            "default": 0,
            "minimum": 0,
            "title": "The unix timestamp of message creation",
            "examples": [
                1589788888888
            ]
        },
        "count": {
            "type": "integer",
            "default": 0,
            "minimum": 0,
            "title": "The amount of items counted",
            "examples": [
                1
            ]
        },
        "scrap": {
            "type": "integer",
            "default": 0,
            "minimum": 0,
            "title": "The optional amount of defective items",
            "examples": [
                0
            ]
        }
    },
    "examples": [{
      "timestamp_ms": 1589788888888,
      "count": 1,
      "scrap": 0
    },{
      "timestamp_ms": 1589788888888,
      "count": 1
    }]
}
```

## Producers

- Typically Node-RED

## Consumers

- [kafka-to-postgresql](/docs/core/kafka-to-postgresql)
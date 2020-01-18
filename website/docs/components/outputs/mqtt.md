---
title: mqtt
type: output
---

```yaml
mqtt:
  client_id: benthos_output
  max_in_flight: 1
  password: ""
  qos: 1
  topic: benthos_topic
  urls:
  - tcp://localhost:1883
  user: ""
```

Pushes messages to an MQTT broker.

The `topic` field can be dynamically set using function interpolations
described [here](/docs/configuration/interpolation#functions). When sending batched
messages these interpolations are performed per message part.

This output benefits from sending multiple messages in flight in parallel for
improved performance. You can tune the max number of in flight messages with the
field `max_in_flight`.


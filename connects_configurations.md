# Connects Configurations

### 1. File Streaming Source

    {
        "connector.class": "org.apache.kafka.connect.file.FileStreamSourceConnector",
        "file": "openrecipes.json",
        "tasks.max": "1",
        "name": "local-file-source",
        "topic": "finance"
    }

| Config | Request | Default | Comments |
| -- | -- | -- | -- |
| **group.id** | Optional | df_trans_flink_group_id | Kafka consumer id.|
| **data.format.input** | Optional | json | Available value are "json_string" and "json". | 
| **data.format.output** |Optional | json | Available value are "json_string" and "json".**[*]**| 
| **avro.schema.enabled** |Optional | false | Whether AVRO schema is enabled in Kafka Connect. | 
| **column.name.list** |Yes | N/A | The list of column names output to Kafka topic. | 

### 2. File Streaming Sink

    {
        "connector.class": "org.apache.kafka.connect.file.FileStreamSinkConnector",
        "file": "openrecipes_sink.json",
        "tasks.max": "1",
        "name": "local-file-sink",
        "topics": "finance"
    }


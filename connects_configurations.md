# Connects Configurations

### 1. File Streaming Source

    {
        "connector.class": "org.apache.kafka.connect.file.FileStreamSourceConnector",
        "file": "openrecipes.json",
        "tasks.max": "1",
        "name": "local-file-source",
        "topic": "finance"
    }

### 2. File Streaming Sink

    {
        "connector.class": "org.apache.kafka.connect.file.FileStreamSinkConnector",
        "file": "openrecipes_sink.json",
        "tasks.max": "1",
        "name": "local-file-sink",
        "topic": "finance"
    }


# 10.03. Grafana

конфиг тут: https://github.com/yuggoth/10-monitoring-03-grafana/blob/main/prometheus.yml

Утилизация CPU для nodeexporter (в процентах, 100-idle)

100 - (avg by (instance) (rate(node_cpu_seconds_total{job="node_exporter",mode="idle"}[1m])) * 100)


CPULA 1/5/15

node_load1{instance="localhost:9100", job="node_exporter", label="<label_1>"}

node_load5{instance="localhost:9100", job="node_exporter", label="<label_1>"}

node_load15{instance="localhost:9100", job="node_exporter", label="<label_1>"}


Количество свободной оперативной памяти

node_memory_MemFree_bytes{instance="localhost:9100", job="node_exporter", label="<label_1>"}


Количество места на файловой системе

node_filesystem_avail_bytes

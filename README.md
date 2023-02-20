to run: docker-compose up -d

In Grafana it is necessary add data source Prometheus

Grafana         latest   ports: "3000:3000"
Prometheus      latest   ports: "9090:9090"
node-exporter   latest   ports: "9100:9100"
MySQL           5.7      ports: "3306:3306"
mysql-exporter  latest   ports: "9104:9104"
phpMyAdmin      latest   ports: "8081:80"
NGINX           latest   ports: "80:80"
GitLab          latest   ports: "90:80"
PlantUML        latest   ports: "9999:8080"
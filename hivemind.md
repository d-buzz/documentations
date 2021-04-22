## Running hivemind image

```docker run -d --name hivemind --env DATABASE_URL=postgresql://postgres:REPLACE_PASSWORD@172.17.0.1:5432/hive --env STEEMD_URL='{"default":"https://apinode"}' --env SYNC_SERVICE=1 -p 8094:8094 hive/hivemind-deathwing:latest```

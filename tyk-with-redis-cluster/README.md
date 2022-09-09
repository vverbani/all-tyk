# Redis cluster with Tyk

The purpose of this repo is to have the correct files and file configurations to enable a Redis Cluster inside of a Tyk instance. This repo is not built to work as a standalone but rather compliment Tyk Pro Docker Demo.

Replace the files inside of this repo into their respective counterparts inside of the Tyk Pro Docker Demo repo:

1. docker-compose.yml --> tyk-pro-docker-demo/docker-compose.yml
2. tyk_analytics.conf --> /confs/tyk_analytics.conf
3. tyk.conf           --> /confs/tyk.conf

## Troubleshooting Tips

1. Depending on system resources there is a slight chance of a racing condition. Redis cluster needs to be up prior to Tyk for a valid connection. If your gateway isn't properly connecting to your dashboard, please restart your Dashboard: `docker-compose restart tyk-dashboard`
2. Make sure your using the correct Tyk component versions inside of `docker-compose.yml`
3. Make sure that Redis version is also aligned with a support version for Tyk.
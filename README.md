# docker-mssql-tailscale

1. For private/dev environment: `sudo mkdir /var/mssql1 && sudo chown 10001:10001 /var/mssql1 && sudo chmod 770 /var/mssql1`. For server/prod environment, consider file permissions as appropriate.
1. The Tailscale authkey and SQL sa password are read from file `.env`. Copy `env-sample` to `.env` and update the values.
1. Run `docker compose up -d` to create & start the containers
1. Run `docker compose down` to remove the containers and keep the data files in `/var/mssql1`
1. Access the SQL Server over the tailnet as `mssql1.[tailnet-domain].ts.net`

### Authkey

To renew the Tailscale authkey, go to Settings ! Personal Settings | Keys. 
Select Generate Auth Key, add description, set for 90 days; enable Tags, then add tag:container

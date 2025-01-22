# docker-mssql-tailscale

1. For private/dev environment: `sudo mkdir /var/mssql && sudo chown 10001:10001 /var/mssql && sudo chmod 770 /var/mssql`. For server/prod environment, consider file permissions as appropriate.
1. The Tailscale authkey and SQL sa password are read from file `.env`. Copy `env-sample` to `.env` and update the values.
1. Run `docker compose up -d` to create & start the containers
1. Run `docker compose down` to remove the containers and keep the data files in `/var/mssql`
1. Access the SQL Server over the tailnet as `mssql1.[tailnet-domain].ts.net`

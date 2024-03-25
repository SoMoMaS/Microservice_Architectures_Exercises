# Prerequisite:
- Having Docker installed

# First time running:

Stand in the root of the project and run docker compose up.
In localhost:9090 you can find the Prometheus running. You need to check that at least one of your targets is up.
In localhost:8082 you can find the exposed api with the front end, and in localhost:8082/metrics you can find the metrics collected from the api.
In localhost:3000 you can find Grafana running. The default user is admin and the password is admin. To create the dashboard for the first time, you need to create a new dashboard and select the metrics. The one called lifetimeRequests counts the number of calls since the docker was first turned on. The one called requestsPerFetch has the number of requests since the localhost:8082/metrics endpoint has been called.  After you create these two visualizations with anyone else you need it is necessary, you have to save the dashboard so that the next time, you already have these visualizations available.

# Running after the first time:

Stand in the root of the project and run docker compose up.
If you have saved the Grafana dashboard, all the visualizations will be visible, if you have not saved it, you will have to configure it again. 
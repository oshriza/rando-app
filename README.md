Kubernetes Logging Exercise
---------------------------
The goal of today's exercise is to deploy the EFK stack to our Kubernetes cluster and use it to create a dashboard for the Rando app.

The Rando app
-------------
Rando is an app that creates logs containing random colors and numbers, it is available here: https://gitlab.com/aransh/rando
Along with it you can find a Helm chart and an optional `random.yaml` values file used to configure Rando to create a random amount of logs at a random interval.

The work plan
-------------
1. Install the EFK stack onto your cluster (use official Helm charts!).
   Note:
   - It's OK to deploy ElasticSearch with only a single master node for the purposes of this task.
   - A values file configured to allow Fluentd to correctly parse JSON logs is attached to the task. You may need to use it.

2. Install the Rando app onto your cluster using Helm.

3. Learn how to query Kibana - write a KQL query to get all Rando's logs (try to be specific!). Save the query.

4. Create a dashboard with Rando app logs' visualizations - Explore the different visualization types to try and make sense of your data (most common number, total randos count, pie-chart of colors, randos/time graph, etc... be creative!).
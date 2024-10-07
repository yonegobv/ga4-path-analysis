# GA4 path analysis

This is a Dataform repository I am working on to model GA4 data in BigQuery in order to do analysis of user path behavior through a website. I am in the process of writing more detailed explanations/documentation, but for now use at your own risk. If you haven't used Dataform, [start here](https://cloud.google.com/dataform).

## To create your own Dataform repository from this repository:
* [Fork this repository](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo).
* [Create your own Dataform repository](https://cloud.google.com/dataform/docs/create-repository).
* [Connect your Dataform repository to your fork of my repository](https://cloud.google.com/dataform/docs/connect-repository).
* [Create a development workspace in Dataform](https://cloud.google.com/dataform/docs/create-workspace#create-workspace).
* Update the variables in the includes/constants.js file.
* Update the defaultProject and defaultLocation variable in the workflow_settings.yaml file. The defaultLocation represents the default BigQuery location to use.
* If you would like to backfill data, change the start_date value in sequenced_events.sqlx and execute all actions from the development workspace. Change the value by increasing the interval value from 2 to however many days you would like to backfill. Change it back once backfilled.
* [Create release and workflow configurations](https://cloud.google.com/dataform/docs/quickstart-schedule-production-execution) to schedule daily executions of the queries.

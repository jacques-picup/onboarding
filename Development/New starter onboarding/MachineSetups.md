## Software installation
To get going, install the following software:
* Visual Studio 2022 (community edition is fine)
* Visual Studio Code
* SQL Server Developer Edition
* SSMS
* .Net 8
* .Net 7 (although this is out of support * currently)
* .Net Framework 4.7.1
* git
* Node (14, 18, 20)
* ng-rok
* eventstore

## Cloning the repositories
You will be assigned to various teams that contain the repositories required to complete your work

The front-end team will have access to the following:
1. PicupTechnologies/enterprise-frontend
1. PicupTechnologies/kl-admin
1. PicupTechnologies/firebase-functions
1. PicupTechnologies/kl-financials
1. PicupTechnologies/kl-zones
1. PicupTechnologies/kl-driver-management
1. PicupTechnologies/kl-host
1. PicupTechnologies/kl-auth
1. PicupTechnologies/kl-reports
1. PicupTechnologies/kl-template
1. PicupTechnologies/kl-post-dispatch
1. PicupTechnologies/cartrack-tracker
1. PicupTechnologies/client-order-widget
1. PicupTechnologies/enterprise-angular
1. PicupTechnologies/order-management-module
1. PicupTechnologies/parcel-ninja-scanning-app
1. PicupTechnologies/picup-admin
1. PicupTechnologies/picup-live-chat-module

The backend team will have access to the following:
1. PicupTechnologies/Billing
1. PicupTechnologies/billing-module-background-jobs
1. PicupTechnologies/billing-module-kafka-consumers
1. PicupTechnologies/billing-module-web-api
1. PicupTechnologies/data-maintenance
1. PicupTechnologies/enterprise-frontend
1. PicupTechnologies/firebase-functions
1. PicupTechnologies/GrafanaDashboards
1. PicupTechnologies/integration-boilerplate
1. PicupTechnologies/Karooooo.AccessManagement
1. PicupTechnologies/Karooooo.AutomatedReportSheduler
1. PicupTechnologies/Karooooo.AutomaticWebhookRequeue
1. PicupTechnologies/Karooooo.CI.DevOps.Example
1. PicupTechnologies/Karooooo.CI.Example
1. PicupTechnologies/Karooooo.Common
1. PicupTechnologies/Karooooo.Common.Confluent
1. PicupTechnologies/Karooooo.Common.Domain
1. PicupTechnologies/Karooooo.Common.Hangfire
1. PicupTechnologies/Karooooo.Common.Hosting
1. PicupTechnologies/Karooooo.Common.Http
1. PicupTechnologies/Karooooo.Common.Logging
1. PicupTechnologies/Karooooo.Common.MsSql
1. PicupTechnologies/Karooooo.Common.OutboxJobs
1. PicupTechnologies/Karooooo.Common.Web
1. PicupTechnologies/Karooooo.Costing
1. PicupTechnologies/Karooooo.CourierIntegration.WebApi
1. PicupTechnologies/Karooooo.Financials
1. PicupTechnologies/Karooooo.Financials.Reporting
1. PicupTechnologies/Karooooo.Financials.V2Events
1. PicupTechnologies/Karooooo.KafkaConsumerBase
1. PicupTechnologies/Karooooo.KpiEvents
1. PicupTechnologies/Karooooo.OrderIngestion
1. PicupTechnologies/Karooooo.PeachPayments.Driver
1. PicupTechnologies/Karooooo.PostgreSql
1. PicupTechnologies/Karooooo.Quoting
1. PicupTechnologies/Karooooo.Reporting
1. PicupTechnologies/Karooooo.Reporting.WebAPI
1. PicupTechnologies/Karooooo.Routing
1. PicupTechnologies/Karooooo.WebhookQueueProcessorUpgrade
1. PicupTechnologies/Karooooo.WebhookV2QueueProcessor
1. PicupTechnologies/picup-admin
1. PicupTechnologies/picup-backend
1. PicupTechnologies/picup-billing
1. PicupTechnologies/picup-billing-module
1. PicupTechnologies/picup-courier-integration
1. PicupTechnologies/picup-kafka-sql-read-model-consumer
1. PicupTechnologies/picup-mono
1. PicupTechnologies/picup-node
1. PicupTechnologies/picup-pdf-library
1. PicupTechnologies/picup-planning-module
1. PicupTechnologies/picup-services
1. PicupTechnologies/picup-shared-auth
1. PicupTechnologies/picup-shared-database
1. PicupTechnologies/Picup.Common.Http.Rfc9457
1. PicupTechnologies/Picup.ParcelTrack
1. PicupTechnologies/Picup.Reporting
1. PicupTechnologies/Picup.Webhooks.WebApi
1. PicupTechnologies/POSTCallLoadTester
1. PicupTechnologies/report-notebooks
1. PicupTechnologies/Shopify
1. PicupTechnologies/woocommerce-picup-shipping

The mobile development team has access to:
1. PicupTechnologies/enterprise-frontend 
1. PicupTechnologies/firebase-functions
1. PicupTechnologies/picup-admin
1. PicupTechnologies/picup-live-chat-module


Other repos not specifically grouped:
1. PicupTechnologies/flutter_paystack
1. PicupTechnologies/launch_review
1. PicupTechnologies/picup-magento-publish
1. PicupTechnologies/picup-php-api
1. PicupTechnologies/ssh-deploy

# Setup eventstore
Copy the eventstore folder to your local machine
suggested: `C:\eventstore` or within your user folder

Edit the EventStore - v2_0.cmd file to reflect the folder that you just created
```
cd C:\EventStore\EventStore-OSS-Win-v5.0.10
EventStore.ClusterNode.exe --run-projections=all --db C:\eventstore\picup-db --log C:\Users\{userName}\DB\EventStore\picup-logs
```

# Setup ng-rok


# Initial run
When you run the solution the first time, there might be some errors and warnings in the IDE regarding nuget packages.
Add the picup nuget package to the Nuget Package Manager
The URI is: `picupnuget.azurewebsites.net/api/v2`

To resolve the types error, mentioned above, run the following from the Nuget Package manager console:
`Update-Package -reinstall`

At this point, you should already have a configuration created for you, if you don't ask someone for assitance.

Choose a default configuration for the first run i.e. `Debug`
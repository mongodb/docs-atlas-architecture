.. code-block:: 
   :copyable: true

   resource "mongodbatlas_alert_configuration" "test" {
     project_id = "PROJECT ID"
     event_type = "NO_PRIMARY"
     enabled    = true

     notification {
       type_name     = "PROMETHEUS"
       integration_id = data.mongodbatlas_third_party_integration.prometheus.id
     }

     notification {
       type_name     = "DATADOG"
       integration_id = data.mongodbatlas_third_party_integration.datadog.id
     }

     matcher {
       field_name = "REPLICA_SET_NAME"
       operator   = "EQUALS"
      value      = "myReplSet"
     }

     threshold_config {
       operator    = "GREATER_THAN"
       threshold   = 24
       units       = "HOURS"
     }
   }
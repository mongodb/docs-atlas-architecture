.. code-block::
   :copyable: true

   resource "mongodbatlas_alert_configuration" "test" {
     project_id = mongodbatlas_project.atlas-project.id
     event_type = "REPLICATION_OPLOG_WINDOW_RUNNING_OUT"
     enabled    = true

     notification {
       type_name     = "GROUP"
       interval_min  = 5
       delay_min     = 0
       sms_enabled   = false
       email_enabled = true
       roles         = ["GROUP_CLUSTER_MANAGER"]
     }

     matcher {
       field_name = "CLUSTER_NAME"
       operator   = "EQUALS"
       value      = "myCluster"
     }

     metric_threshold_config {
       operator    = "LESS_THAN"
       threshold   = 1
       units       = "HOURS"
     }
   }
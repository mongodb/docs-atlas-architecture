.. code-block:: 
   :copyable: true 

   resource "mongodbatlas_cloud_backup_schedule" "test" {  
     project_id    = mongodbatlas_advanced_cluster.my_cluster.project_id  
     cluster_name  = mongodbatlas_advanced_cluster.my_cluster.name 
      
     reference_hour_of_day    = 3  # time of backup
     reference_minute_of_hour = 45 # time of backup 
     restore_window_days      = 4  # backup retention in days
  
     copy_settings {  
       cloud_provider = "AWS"  # Cloud provider for backup
       frequencies = ["HOURLY", "DAILY", "WEEKLY", "MONTHLY", "YEARLY", "ON_DEMAND"]  
       region_name        = "US_EAST_1"  # backup region
       zone_id            = mongodbatlas_advanced_cluster.myCluster.replication_specs.*.zone_id[0]  # cluster's zone ID from the replication specs
       should_copy_oplogs = true  # enables copy of oplogs
     }  
  
     policy_item_hourly {  
       frequency_interval = 1  
       retention_unit     = "days"  
       retention_value    = 4  
     }  
     policy_item_daily {  
       frequency_interval = 1  
       retention_unit     = "days"  
       retention_value    = 4  
     }  
     policy_item_weekly {  
       frequency_interval = 4  
       retention_unit     = "weeks"  
       retention_value    = 4  
     }  
     policy_item_monthly {  
       frequency_interval = 5  
       retention_unit     = "months"  
       retention_value    = 4  
     }  
     policy_item_yearly {  
       frequency_interval = 1  
       retention_unit     = "years"  
       retention_value    = 4  
     }  
   }

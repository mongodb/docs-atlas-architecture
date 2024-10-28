.. code-block:: shell 
   :copyable: true

   resource "mongodbatlas_database_user" "admin_user" {
     username = "adminUser"
     password = "securePassword"  # Use a secure password
     auth_database_name = "admin"

     roles {
       role_name     = "atlasAdmin"  # Admin role for the cluster
       database_name = "admin"
     }

     roles {
       role_name     = "projectOwner"  # Project member rights
       database_name = "admin"
     }
   }

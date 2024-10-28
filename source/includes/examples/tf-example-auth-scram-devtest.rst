.. code-block:: shell 
   :copyable: true 

   resource "mongodbatlas_database_user" "example_user" {
     username = "exampleUser"
     password = "examplePassword"  # Use a secure password
     auth_database_name = "admin"
     roles {
       role_name     = "readWriteAny"
       database_name = "exampleDatabase"
     }
     scopes {
       database_name = "exampleDatabase"
       collection_name = ""
     }
   }

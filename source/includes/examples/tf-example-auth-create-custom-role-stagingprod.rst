.. code-block:: 
   :copyable: true 

   resource "mongodbatlas_custom_db_role" "create_role" {
     project_id = "56fd11f25f23b33ef4c2a331"
     role_name  = "my_custom_role"

     actions {
       action = "UPDATE"
       resources {
         collection_name = ""
         database_name   = "myDb"
       }
     }
     actions {
       action = "INSERT"
       resources {
         collection_name = ""
         database_name   = "myDb"
       }
     }
     actions {
       action = "REMOVE"
       resources {
         collection_name = ""
         database_name   = "myDb"
       }
     }
   }
.. code-block:: 
   :copyable: true 

   resource "mongodbatlas_database_user" "test" {
     username           = "64d613677e1ad50839cce4db/testUserOr"
     project_id         = "6414908c207f4d22f4d8f232"
     auth_database_name = "admin"
     oidc_auth_type     = "IDP_GROUP"

     roles {
       role_name     = "readWriteAnyDatabase"
       database_name = "admin"
     }
   }
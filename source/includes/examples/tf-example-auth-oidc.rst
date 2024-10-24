.. code-block:: 
   :copyable: true 

   resource "mongodbatlas_federated_settings_identity_provider" "oidc" {
     federation_settings_id = data.mongodbatlas_federated_settings.this.id
     audience               = var.token_audience
     authorization_type     = "USER"
     description            = "oidc"
     issuer_uri = "https://sts.windows.net/${azurerm_user_assigned_identity.this.tenant_id}/"
     idp_type   = "WORKLOAD"
     name       = "OIDC-for-azure"
     protocol   = "OIDC"
     user_claim = "sub"
   }
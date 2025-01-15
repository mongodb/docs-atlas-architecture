For staging and production environments, we recommend that you enable :ref:`BYOK
encryption <security-kms-encryption>` through AWS Key Management Service (KMS), 
Google Cloud KMS, or Azure Key Vault when provisioning your {+clusters+} 
to avoid relying on application development teams to configure it later on. 
This also ensures consistent data protection across your environments.

For development and testing environments, consider skipping |byok| encryption
to save costs. However, if you're storing sensitive data in |service|, 
such as for healthcare or financial services industries, consider enabling 
|byok| encryption in development and testing environments as well.

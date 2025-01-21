
:ref:`BYOK encryption <arch-center-encryption-at-rest>` is enabled at the project level. 
Once enabled, it automatically applies to all {+clusters+} created within the project, 
ensuring consistent data protection across your environment.

For **staging and production environments**, we recommend that you 
enable BYOK encryption when provisioning your {+clusters+} 
to avoid relying on application development teams to configure it later on.

For **development and testing environments**, consider skipping |byok| encryption
to save costs. However, if you're storing sensitive data in |service|, 
such as for healthcare or financial services industries, consider enabling 
|byok| encryption in development and testing environments as well.

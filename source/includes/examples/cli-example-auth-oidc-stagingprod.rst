.. code-block:: 
   :copyable: true 

   atlas federatedAuthentication federationSettings identityProvider create oidc IDPName \ 
     --audience "audience" \ 
     --authorizationType "GROUP" \
     --clientId clientId \
     --desc "IDPName test" \
     --federationSettingsId "5d1113b25a115342acc2d1aa" \
     --groupsClaim "groups" \
     --idpType "WORKLOAD" \
     --issuerUri uri" \
     --userClaim "user"  \
     --associatedDomain "domain"
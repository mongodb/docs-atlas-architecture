.. io-code-block:: 
   :copyable: true 

   .. input:: 
      :language: sh 

      atlas auditing describe --output json

   .. output:: 
      :language: sh 
      :visible: false

      {
        "auditAuthorizationSuccess": false,
        "auditFilter": "{\"atype\":\"authorization\"}",
        "configurationType": "FILTER_JSON",
        "enabled": true
      }

.. code-block::
   :copyable: true

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-portal-prod
   spec:
     name: Customer Portal - Prod
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-portal-test
   spec:
     name: Customer Portal - Test
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-portal-dev
   spec:
     name: Customer Portal - Dev
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF


   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-pmapp-prod
   spec:
     name: PM App - Prod
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-pmapp-test
   spec:
     name: PM App - Test
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasProject
   metadata:
     name: project-pmapp-dev
   spec:
     name: PM App - Dev
     projectIpAccessList:
       - ipAddress: <your-ip-address-range>
         comment: "Adding your IP to Atlas access list"
   EOF
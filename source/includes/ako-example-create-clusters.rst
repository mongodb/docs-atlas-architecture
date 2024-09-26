.. code-block::
   :copyable: true

   cat <<EOF | kubectl apply -f -
   apiVersion: atlas.mongodb.com/v1
   kind: AtlasDeployment
   metadata:
     name: cluster-portal-prod
     namespace: mongodb-atlas-system
   spec:
     projectRef:
       name: project-portal-prod
     deploymentSpec:
       clusterType: REPLICASET
       name: "Cluster Portal - Prod"
       tags:
       - key: "environment"
         value: "production"
       backupEnabled: true
       replicationSpecs:
         - regionConfigs:
           - electableSpecs:
               instanceSize: M10
               nodeCount: 3
             providerName: AWS
             regionName: US_EAST_1
             priority: 7
           - electableSpecs:
               instanceSize: M10
               nodeCount: 2
             providerName: AZURE
             regionName: US_EAST_2
             priority: 6
           - electableSpecs:
               instanceSize: M10
               nodeCount: 2
             providerName: GCP
             regionName: CENTRAL_US
             priority: 5
   EOF
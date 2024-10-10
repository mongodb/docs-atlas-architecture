.. code-block::
   :copyable: true

   curl --user "{PUBLIC-KEY}:{PRIVATE-KEY}" --digest \
      --header "Content-Type: application/json" \
      --header "Accept: application/vnd.atlas.2023-02-01+json" \
      --include \
      --request POST "https://cloud.mongodb.com/api/atlas/v2/groups/56fd11f25f23b33ef4c2a331/clusters" \
      --data '
 {
  "backupEnabled": false,
  "clusterType": "REPLICASET",
  "labels": [],
  "links": [],
  "mongoDBMajorVersion": "8.0",
  "name": "CustomerPortalDev",
  "replicationSpecs": [
    {
      "id": "6706bf6c586d634be7ef9e37",
      "numShards": 1,
      "regionConfigs": [
        {
          "electableSpecs": {
            "instanceSize": "M30",
            "nodeCount": 3
          },
          "priority": 7,
          "providerName": "GCP",
          "regionName": "EASTERN_US",
          "analyticsSpecs": {
            "nodeCount": 0,
            "instanceSize": "M30"
          },
          "autoScaling": {
            "compute": {
              "enabled": false,
              "scaleDownEnabled": false
            },
            "diskGB": {
              "enabled": false
            }
          },
          "readOnlySpecs": {
            "nodeCount": 0,
            "instanceSize": "M30"
          }
        }
      ],
      "zoneName": "Zone 1"
    }
  ],
  "tags": [],
  "terminationProtectionEnabled": false,
}
.. code-block::
   :copyable: true

   curl --user "{PUBLIC-KEY}:{PRIVATE-KEY}" --digest \
         --header "Content-Type: application/json" \
         --header "Accept: application/vnd.atlas.2023-02-01+json" \
         --include \
         --request POST "https://cloud.mongodb.com/api/atlas/v2/groups/{groupId}/clusters" \
         --data '
            {
              "clusterType": "SHARDED",
              "name": "myCluster",
              "replicationSpecs": [
                {
                  "regionConfigs": [
                    {
                      "analyticsAutoScaling": {
                        "autoIndexing": {
                          "enabled": false
                        },
                        "compute": {
                          "enabled": false
                        },
                        "diskGB": {
                          "enabled": true
                        }
                      },
                      "analyticsSpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M30",
                        "nodeCount": 0
                      },
                      "autoScaling": {
                        "autoIndexing": {
                          "enabled": false
                        },
                        "compute": {
                          "enabled": false
                        },
                        "diskGB": {
                          "enabled": true
                        }
                      },
                      "electableSpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M30",
                        "nodeCount": 3
                      },
                      "priority": 7,
                      "providerName": "AWS",
                      "readOnlySpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M30",
                        "nodeCount": 0
                      },
                      "regionName": "US_EAST_1"
                    }
                  ],
                  "zoneName": "Zone 1"
                },
                {
                  "regionConfigs": [
                    {
                      "analyticsAutoScaling": {
                        "autoIndexing": {
                          "enabled": false
                        },
                        "compute": {
                          "enabled": false
                        },
                        "diskGB": {
                          "enabled": true
                        }
                      },
                      "analyticsSpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M10",
                        "nodeCount": 0
                      },
                      "autoScaling": {
                        "autoIndexing": {
                          "enabled": false
                        },
                        "compute": {
                          "enabled": false
                        },
                        "diskGB": {
                          "enabled": true
                        }
                      },
                      "electableSpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M10",
                        "nodeCount": 3
                      },
                      "priority": 7,
                      "providerName": "AWS",
                      "readOnlySpecs": {
                        "diskSizeGB": 10,
                        "instanceSize": "M10",
                        "nodeCount": 0
                      },
                      "regionName": "US_EAST_1"
                    }
                  ],
                  "zoneName": "Zone 1"
                }
              ]
            }'



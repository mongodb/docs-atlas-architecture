.. code-block::
   :copyable: true

   curl --user "{PUBLIC-KEY}:{PRIVATE-KEY}" --digest \
         --header "Content-Type: application/json" \
         --header "Accept: application/vnd.atlas.2023-02-01+json" \
         --include \
         --request POST "https://cloud.mongodb.com/api/atlas/v2/groups" \
         --data '
            {
              "name": "Customer Portal - Prod",
              "orgId": "32b6e34b3d91647abb20e7b8",
              "tags": [
                {
                  "key": "environment",
                  "value": "production"
                }
              ],
              "withDefaultAlertsSettings": true
            }'



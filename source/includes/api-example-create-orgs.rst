.. code-block::
   :copyable: true

   curl --user "{PUBLIC-KEY}:{PRIVATE-KEY}" --digest \
         --header "Content-Type: application/json" \
         --header "Accept: application/vnd.atlas.2023-02-01+json" \
         --include \
         --request POST "https://cloud.mongodb.com/api/atlas/v2/orgs" \
         --data '
            {
              "apiKey": {
                "desc": "OrgOwnerKey",
                "roles": [
                  "ORG_OWNER"
                ]
              },
              "name": "Consumer Products Business Unit Org",
              "orgOwnerId": "32b6e34b3d91647abb20e7b8"
            }'



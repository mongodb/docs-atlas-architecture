.. code-block::
   :copyable: true

   atlas clusters create CustomerPortalDev \
     --projectId 618d48e05277a606ed2496fe \
     --region EASTERN_US \
     --members 3 \
     --tier M10 \
     --provider GCP \
     --mdbVersion 8.0 \
     --diskSizeGB 30 \
     --tag bu=ConsumerProducts \
     --tag teamName=TeamA \
     --tag appName=ProductManagementApp \
     --tag env=Production \
     --tag version=8.0 \
     --tag email=marissa@acme.com \
     --watch

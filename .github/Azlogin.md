
   az ad sp create-for-rbac --name "myApp" --role contributor \
                            --scopes /subscriptions/{subscription-id}/resourceGroups/{resource-group} \
                            --sdk-auth
                            
  # Replace {subscription-id}, {resource-group} with the subscription, resource group details

    subscription-id : 07a9a2a5-ceb6-4b0b-b356-094a827d0ace
    resource-group : openhackl983v804rg


       az ad sp create-for-rbac --name "openhack" --role contributor \
                            --scopes /subscriptions/07a9a2a5-ceb6-4b0b-b356-094a827d0ace/resourceGroups/openhackl983v804rg \
                            --sdk-auth


  # The command should output a JSON object similar to this:

  {
    "clientId": "<GUID>",
    "clientSecret": "<GUID>",
    "subscriptionId": "<GUID>",
    "tenantId": "<GUID>",
    (...)
  }

  {
  "clientId": "251ddb8b-6432-4fa8-909a-213f4314de4a",
  "clientSecret": "hg35rUER_8.qYfihx15s5xzLf8ztJoanQ7",
  "subscriptionId": "07a9a2a5-ceb6-4b0b-b356-094a827d0ace",
  "tenantId": "04a9dc15-17e4-4f47-9e5d-e528f7797b15",
  "activeDirectoryEndpointUrl": "https://login.microsoftonline.com",
  "resourceManagerEndpointUrl": "https://management.azure.com/",
  "activeDirectoryGraphResourceId": "https://graph.windows.net/",
  "sqlManagementEndpointUrl": "https://management.core.windows.net:8443/",
  "galleryEndpointUrl": "https://gallery.azure.com/",
  "managementEndpointUrl": "https://management.core.windows.net/"
}
  
# Example email to participants

Hello everyone,

I hope you are excited for our upcoming JBoss EAP migration workshop! Before the workshop, please do the following:

1. Go to the [Azure Pass site](https://www.microsoftazurepass.com/) to redeem your code, which will create a new Azure Subscription. Your Azure Pass code is **XXX-XXX-XXX-XXX**.
2. Go to [this GitHub repository](https://github.com/Azure-Samples/workshop-migrate-jboss-on-app-service) and make a fork of it in your personal GitHub account.
3. On the night before the workshop, run the following Azure CLI command to create a few big resources that we will need in the workshop. This deployment will take 2-3 hours to complete.

    ```bash
    LOCATION=eastus
    RESOURCE_GROUP=jboss-rg
    az group create --name $RESOURCE_GROUP --location $LOCATION
    az deployment group create \
        --name ase_deployment \
        --resource-group $RESOURCE_GROUP \
        --template-uri https://raw.githubusercontent.com/Azure-Samples/workshop-migrate-jboss-on-app-service/main/templates/ase-template.json \
        --no-wait \
        --parameters webAppName=jboss-ilb-ase
    ```

    > If you do not have the Azure CLI installed, you can log into Azure and use the [Cloud Shell](https://shell.azure.com/)

Contact me if you have any questions!

Best,
*YOUR NAME HERE*
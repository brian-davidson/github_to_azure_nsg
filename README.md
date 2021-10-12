This GitHub action allows a hosted(public) runner image to access resources secured by an Azure Network Security Group (NSG) by creating an allow rule picking the current IP address of the hosted runner, also the same task can be used to remove existing NSG rules allowing the cleanup of the created rules.

E.g. Web Deploy to a WebApp inside an Azure Application Service Environment (ASE)
Inputs
azure-credentials

    Required SPN details as secrets.AZURE_CREDENTIALS, Refer Configure Azure Credentials on how to.
    Default "N/A".

rule-priority-start:

    Optional Start value for the priority range to be used.
    Default "300".

rule-priority-range:

    Optional range of the NSG priority values to be used when multiple agents are deploying sharing the same NSG.
    Default "100".

rule-inbound-port:

    Optional Port for the inbound rule'.
    Default "443".

rule-id-for-removal:

    Optional rule id to remove. If this value is defined the action will default to deleteing.
    Default "".

rule-nsg-resource-group-name:

    Required Resource Group of the NSG.
    Default "N/A".

rule-nsg-name:

    Required Name of the NSG.
    Default "N/A".

Outputs



## ConnectToAzureWithSPN

#IN Powershell 

$SPAplicationId ="ba3ef1c4-92b4-4b38-b69f-89b39314d87a"
$TenantId= "UR Tenant ID"
$Password = ConvertTo-SecureString KSRxe70SfCbr.r89mv-KXc2_2T29x-DWtw -AsPlainText -Force
$psCred = New-Object System.Management.Automation.PSCredential($SPAplicationId , $Password)

Connect-AzAccount -Credential $psCred -TenantId $azureTenantId  -ServicePrincipal -Subscription YOURSUBSCRIPTIONID

# IN AUTOMATION


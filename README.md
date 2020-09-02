# ConnectToAzureWithSPN


## I Will Show, how to Connect to Azure Using Service Princple with Powershell



Here is the Windows PS Script.

$SPAplicationId ="ba3ef1c4-92b4-4b38-b69f-89b39314d87a"
$TenantId= "fd02ec63-37d9-49b6-b6da-af2670ad9e1c"
$Password = ConvertTo-SecureString "KSRxe70SfCbr.r89mv-KXc2_2T29x-DWtw" -AsPlainText -Force
$psCred = New-Object System.Management.Automation.PSCredential($SPAplicationId , $Password)

Connect-AzAccount -Credential $psCred -TenantId $azureTenantId  -ServicePrincipal -Subscription 4c1885b8-7dc3-4bb3-8cfc-ebcb9fefdf3b


## Automate this Process in Automation Account

$SPAplicationId = Get-AutomationVariable -Name 'SPAplicationId'
$TenantId= Get-AutomationVariable -Name 'TenantId'
$Password = ConvertTo-SecureString 'Password' -AsPlainText -Force
$psCred = New-Object System.Management.Automation.PSCredential($SPAplicationId , $Password)


Connect-AzAccount -ServicePrincipal -Credential $psCred -TenantId $TenantId

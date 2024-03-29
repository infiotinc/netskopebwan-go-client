# Go API client for swagger

# Introduction  <b>Infiot</b> provides API endpoints for interacting with <b> Infiot Management Portal</b>, so that you can rapidly deploy IoT at scale anywhere with automation.  <b>Infiot's</b> Developer-friendly SDKs and APIs enable seamless integration.Leverage <b>Infiot SDK</b> and seamlessly integrate with additional services for early time-to-market.  The <b>Infiot API</b> is a powerful [REST API](https://en.wikipedia.org/wiki/Representational_state_transfer) that can be accessed by an [HTTP](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol) client tools such as curl/wget, or HTTP libraries of most modern programming languages including Python, GoLang, Java.  The API provides abundance of features, listing some of the top rated ones, * Support to interact securely with our API Servers from a Client Web application (<b>API tokens should never be exposed outside</b>).  * The API responds with a well-formatted [JSON](http://www.json.org/) data.  * Support for built-in HTTP features, like HTTP authentication and HTTP verbs, which can be easily interpreted by any HTTP clients that are designed to comply with [HTTP RFC](https://tools.ietf.org/html/rfc2616).   If you have good knowledge with REST API, our reference guide will help serve you to get started.  To start using <b>Infiot</b> APIs, API tokens need to be created  If you have any questions you can reach out to us on [support@infiot.com](mailto:support@infiot.com)  # Endpoints  Our APIs can be accessed through HTTP requests to our API Servers. There are different API servers provisioned based on production stages. The user has to select the applicable API server from the given list of servers populated, and punch in the appropriate MSP tenant name field to get started:  ``` https://{tenant}.api.infiot.net ```  All our APIs are [versioned] (#versioning). If there are any changes to the API which either changes the response format or request parameter, the version would be incremented accordingly.  # Authentication  To authenticate your API request you will need to include your secret token. You can manage your API tokens in the Infiot MSP Portal.The user should have appropriate privileges in the tenant portal for the tokens option to be visible.  Tokens can be generated from `Tokens` navigation window.Your API tokens carry many privileges, so be sure to keep them secure. Do not share your secret API tokens in publicly accessible areas such as GitHub, client-side code, and so on.   All API requests must be made over secure HTTP [HTTPS](https://en.wikipedia.org/wiki/HTTPS). Calls made over plain HTTP or without authentication will fail.  Once the token is generated and ready to use, authorize the API token in the swagger hub, click on the `Authorize` button and in the pop-up, fill the API token and click on `Authorize` again.   # Request Methods  Our API endpoints use [HTTP request methods](https://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods) to specify the desired operation to be performed. The documentation below specifies request method supported by each endpoint and the resulting action with its appropriate CRUD workflow.  | Method Type   | CRUD   | Description   | |-  |-  |-  | | GET   | Read   | GET requests can be used to retrieve data (eg: get all tenant details from a Master MSP or MSP)   | | POST   | Create   | POST requests can be used to create a new record (eg: adding new tenants to the Master MSP or MSP)   | | PUT   | Update/Replace   | PUT requests can be used for updating an existing record (eg: updating the name or description of a MSP   | | DELETE   | Delete   | DELETE requests can be used to delete a record (like deleting a MSP from the Master MSP) |   # Response Codes  All API requests will respond with appropriate [HTTP status code](https://en.wikipedia.org/wiki/List_of_HTTP_status_codes). Your API client should handle each response class differently. | Response Code    | Description | |-                 |-            | | 2XX              | These are successful responses and indicate that the API request returned the expected response | | 4XX              | These indicate that there was a problem with the request like a missing parameter or invalid values | |5XX               | These indicate server errors when the server is unreachable or is misconfigured. In this case, you should retry the API request after some delay |   # <a name=\"versioning\"></a>Versioning  All our APIs are versioned. Our current API version is `v1` and we are continuously working on improving it further and provide additional endpoints. If there are any changes to an API which either changes the response format or request parameter, we will increment the version.

## Overview
This API client was generated by the [swagger-codegen](https://github.com/swagger-api/swagger-codegen) project.  By using the [swagger-spec](https://github.com/swagger-api/swagger-spec) from a remote server, you can easily generate an API client.

- API version: v9
- Package version: 1.0.0
- Build package: io.swagger.codegen.v3.generators.go.GoClientCodegen

## Installation
Put the package under your project folder and add the following in import:
```golang
import "./swagger"
```

## Documentation for API Endpoints

All URIs are relative to *https://virtserver.swaggerhub.com/infiot/infiot-api/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*DevicePoliciesApi* | [**AddDevicePolicy**](docs/DevicePoliciesApi.md#adddevicepolicy) | **Post** /devicepolicies | Create new Device Policy
*DevicePoliciesApi* | [**DeleteDevicePolicyById**](docs/DevicePoliciesApi.md#deletedevicepolicybyid) | **Delete** /devicepolicies/{id} | Delete Device policy using policy Id
*DevicePoliciesApi* | [**GetAllDevicePolicies**](docs/DevicePoliciesApi.md#getalldevicepolicies) | **Get** /devicepolicies | List all device policies
*DevicePoliciesApi* | [**GetDevicePolicyById**](docs/DevicePoliciesApi.md#getdevicepolicybyid) | **Get** /devicepolicies/{id} | Get device policy using policy Id
*DevicePoliciesApi* | [**UpdateDevicePolicyById**](docs/DevicePoliciesApi.md#updatedevicepolicybyid) | **Put** /devicepolicies/{id} | Update device policy details using device policy Id
*DevicesApi* | [**AddManagedDevice**](docs/DevicesApi.md#addmanageddevice) | **Post** /edges/{id}/devices | Create new managed device
*DevicesApi* | [**DeleteManagedDeviceById**](docs/DevicesApi.md#deletemanageddevicebyid) | **Delete** /edges/{id}/devices/{deviceId} | Delete Managed Device by Id
*DevicesApi* | [**GetManagedDeviceById**](docs/DevicesApi.md#getmanageddevicebyid) | **Get** /edges/{id}/devices/{deviceId} | Get Managed Device details by Id
*DevicesApi* | [**GetManagedDeviceList**](docs/DevicesApi.md#getmanageddevicelist) | **Get** /edges/{id}/devices | Get list of managed devices
*DevicesApi* | [**GetOnlineDeviceList**](docs/DevicesApi.md#getonlinedevicelist) | **Get** /edges/{id}/onlinedevices | Get list of devices that are currently online
*DevicesApi* | [**UpdateManagedDeviceById**](docs/DevicesApi.md#updatemanageddevicebyid) | **Put** /edges/{id}/devices/{deviceId} | Update Managed Device details by Id
*EdgesApi* | [**ActivateEdgeById**](docs/EdgesApi.md#activateedgebyid) | **Post** /edges/{id}/activate | Create edge activation code
*EdgesApi* | [**AddEdge**](docs/EdgesApi.md#addedge) | **Post** /edges | Create a new edge
*EdgesApi* | [**AddEdgeInterface**](docs/EdgesApi.md#addedgeinterface) | **Post** /edges/{id}/interfaces | Create new interface
*EdgesApi* | [**DeleteEdgeById**](docs/EdgesApi.md#deleteedgebyid) | **Delete** /edges/{id} | Delete Edge by Id value
*EdgesApi* | [**DeleteEdgeIfByName**](docs/EdgesApi.md#deleteedgeifbyname) | **Delete** /edges/{id}/interfaces/{name} | Delete Edge Interface by name
*EdgesApi* | [**GetAllEdges**](docs/EdgesApi.md#getalledges) | **Get** /edges | List all edges
*EdgesApi* | [**GetEdgeById**](docs/EdgesApi.md#getedgebyid) | **Get** /edges/{id} | Get edge by Id value
*EdgesApi* | [**GetEdgeIfByName**](docs/EdgesApi.md#getedgeifbyname) | **Get** /edges/{id}/interfaces/{name} | Get edge&#x27;s interface details by name
*EdgesApi* | [**GetEdgeInterfaceList**](docs/EdgesApi.md#getedgeinterfacelist) | **Get** /edges/{id}/interfaces | Get edge&#x27;s interface list
*EdgesApi* | [**GetEdgeStatusById**](docs/EdgesApi.md#getedgestatusbyid) | **Get** /edges/{id}/status | Get edge last known status by Id value
*EdgesApi* | [**UpdateEdgeById**](docs/EdgesApi.md#updateedgebyid) | **Put** /edges/{id} | Update edge by Id value
*EdgesApi* | [**UpdateEdgeIfByName**](docs/EdgesApi.md#updateedgeifbyname) | **Put** /edges/{id}/interfaces/{name} | Update edge interface details by name
*MonitoringApi* | [**GetGatewayAggregatedDeviceFlowStatsByID**](docs/MonitoringApi.md#getgatewayaggregateddeviceflowstatsbyid) | **Get** /monitoring/gateways/{id}/devices/device_flows_totals | Get gateway device flows aggregated metrics
*MonitoringApi* | [**GetGatewayAggregatedDeviceStatsByID**](docs/MonitoringApi.md#getgatewayaggregateddevicestatsbyid) | **Get** /monitoring/gateways/{id}/devices/devices_totals | Get gateway devices aggregated metrics
*MonitoringApi* | [**GetGatewayAggregatedPathAndLinkStatsByID**](docs/MonitoringApi.md#getgatewayaggregatedpathandlinkstatsbyid) | **Get** /monitoring/gateways/{id}/wan/paths_links_totals | Get gateway paths and links aggregated metrics
*MonitoringApi* | [**GetGatewayLTESignalStatsByID**](docs/MonitoringApi.md#getgatewayltesignalstatsbyid) | **Get** /monitoring/gateways/{id}/system/lte | Get gateway LTE signal time series statistics
*MonitoringApi* | [**GetGatewayLatestInterfaceStatsByID**](docs/MonitoringApi.md#getgatewaylatestinterfacestatsbyid) | **Get** /monitoring/gateways/{id}/overview/interfaces_latest | Get gateway interfaces latest metrics
*MonitoringApi* | [**GetGatewayLatestPathStatsByID**](docs/MonitoringApi.md#getgatewaylatestpathstatsbyid) | **Get** /monitoring/gateways/{id}/overview/paths_latest | Get gateway paths latest metrics
*MonitoringApi* | [**GetGatewayLatestRouteStatsByID**](docs/MonitoringApi.md#getgatewaylatestroutestatsbyid) | **Get** /monitoring/gateways/{id}/overview/routes_latest | Get gateway routes latest metrics
*MonitoringApi* | [**GetGatewayLoadStatsByID**](docs/MonitoringApi.md#getgatewayloadstatsbyid) | **Get** /monitoring/gateways/{id}/system/load | Get gateway system load time series statistics
*MonitoringApi* | [**GetGatewayMemoryStatsByID**](docs/MonitoringApi.md#getgatewaymemorystatsbyid) | **Get** /monitoring/gateways/{id}/system/memory | Get gateway memory time series statistics
*MonitoringApi* | [**GetGatewayPathAndLinkStatsByID**](docs/MonitoringApi.md#getgatewaypathandlinkstatsbyid) | **Get** /monitoring/gateways/{id}/wan/paths_links | Get gateway paths and links time series metrics
*MonitoringApi* | [**GetGatewayUptimeStatsByID**](docs/MonitoringApi.md#getgatewayuptimestatsbyid) | **Get** /monitoring/gateways/{id}/system/uptime | Get gateway uptime time series statistics
*MonitoringApi* | [**GetGatewayWiFiStrengthStatsByID**](docs/MonitoringApi.md#getgatewaywifistrengthstatsbyid) | **Get** /monitoring/gateways/{id}/system/wifi | Get gateway WiFi strength time series statistics
*PoliciesApi* | [**AddDenySourceIPRuleToPolicy**](docs/PoliciesApi.md#adddenysourceipruletopolicy) | **Post** /policies/{id}/block-src-ip | Create new firewall block rule for a specific source IP
*PoliciesApi* | [**AddPolicy**](docs/PoliciesApi.md#addpolicy) | **Post** /policies | Create new policy
*PoliciesApi* | [**AddQoSSourceIPRuleToPolicy**](docs/PoliciesApi.md#addqossourceipruletopolicy) | **Post** /policies/{id}/qos-rule-src-ip | Create new QoS rule for a specific source IP
*PoliciesApi* | [**DeleteDenySourceIPRuleFromPolicy**](docs/PoliciesApi.md#deletedenysourceiprulefrompolicy) | **Delete** /policies/{id}/block-src-ip/{ip} | Delete a policy firewall rule using match source IP
*PoliciesApi* | [**DeletePolicyById**](docs/PoliciesApi.md#deletepolicybyid) | **Delete** /policies/{id} | Delete policy using policy Id
*PoliciesApi* | [**DeleteQoSSourceIPRuleFromPolicy**](docs/PoliciesApi.md#deleteqossourceiprulefrompolicy) | **Delete** /policies/{id}/qos-rule-src-ip/{ip} | Delete a policy QoS rule using match source IP
*PoliciesApi* | [**GetAllPolicies**](docs/PoliciesApi.md#getallpolicies) | **Get** /policies | List all policies
*PoliciesApi* | [**GetPolicyById**](docs/PoliciesApi.md#getpolicybyid) | **Get** /policies/{id} | Get policy using policy Id
*PoliciesApi* | [**UpdatePolicyById**](docs/PoliciesApi.md#updatepolicybyid) | **Put** /policies/{id} | Update policy details using policy Id
*TenantsApi* | [**AddTenant**](docs/TenantsApi.md#addtenant) | **Post** /tenants | Create a new tenant
*TenantsApi* | [**DeleteTenantById**](docs/TenantsApi.md#deletetenantbyid) | **Delete** /tenants/{tenantId} | Delete tenant using tenant Id
*TenantsApi* | [**GetAllTenants**](docs/TenantsApi.md#getalltenants) | **Get** /tenants | List all tenants
*TenantsApi* | [**GetTenantById**](docs/TenantsApi.md#gettenantbyid) | **Get** /tenants/{tenantId} | Get tenant details using tenant Id
*TenantsApi* | [**UpdateTenantById**](docs/TenantsApi.md#updatetenantbyid) | **Put** /tenants/{tenantId} | Update tenant details using tenant Id
*UsersApi* | [**AddUser**](docs/UsersApi.md#adduser) | **Post** /users | Create a new user
*UsersApi* | [**DeleteUserById**](docs/UsersApi.md#deleteuserbyid) | **Delete** /users/{id} | Delete User using user Id
*UsersApi* | [**GetAllUsers**](docs/UsersApi.md#getallusers) | **Get** /users | List all users
*UsersApi* | [**GetUserById**](docs/UsersApi.md#getuserbyid) | **Get** /users/{id} | Get user details using user Id
*UsersApi* | [**UpdateUserById**](docs/UsersApi.md#updateuserbyid) | **Put** /users/{id} | Update user details using user Id

## Documentation For Models

 - [AddDevicePolicyInput](docs/AddDevicePolicyInput.md)
 - [AddEdgeInput](docs/AddEdgeInput.md)
 - [AddPolicyFirewallRuleInput](docs/AddPolicyFirewallRuleInput.md)
 - [AddPolicyInput](docs/AddPolicyInput.md)
 - [AddPolicyQoSRuleInput](docs/AddPolicyQoSRuleInput.md)
 - [AllOfGatewayWanPathsAndLinksStatsData](docs/AllOfGatewayWanPathsAndLinksStatsData.md)
 - [ClientConfiguration](docs/ClientConfiguration.md)
 - [ClientIpv4PoolRangesInner](docs/ClientIpv4PoolRangesInner.md)
 - [CloneIdInput](docs/CloneIdInput.md)
 - [DataUsageLimitSetting](docs/DataUsageLimitSetting.md)
 - [DhcpServerSettings](docs/DhcpServerSettings.md)
 - [DhcpServerSettingsAddressRanges](docs/DhcpServerSettingsAddressRanges.md)
 - [DhcpServerSettingsCustomOptions](docs/DhcpServerSettingsCustomOptions.md)
 - [DhcpServerSettingsMacAddressToIpv4Bindings](docs/DhcpServerSettingsMacAddressToIpv4Bindings.md)
 - [Edge](docs/Edge.md)
 - [EdgeActivationCode](docs/EdgeActivationCode.md)
 - [EdgeBgpConfiguration](docs/EdgeBgpConfiguration.md)
 - [EdgeGenerateActivationCodeInput](docs/EdgeGenerateActivationCodeInput.md)
 - [EdgeModel](docs/EdgeModel.md)
 - [EdgeOverlayConfiguration](docs/EdgeOverlayConfiguration.md)
 - [EdgeOverlayConfigurationRoutableAddresses](docs/EdgeOverlayConfigurationRoutableAddresses.md)
 - [EdgeRef](docs/EdgeRef.md)
 - [EdgeRole](docs/EdgeRole.md)
 - [EdgeStatus](docs/EdgeStatus.md)
 - [EdgeStatusDsDevstatusGeneral](docs/EdgeStatusDsDevstatusGeneral.md)
 - [EdgeStatusDsDevstatusGeneralDsgGeolocation](docs/EdgeStatusDsDevstatusGeneralDsgGeolocation.md)
 - [EdgeStatusDsFlowcounts](docs/EdgeStatusDsFlowcounts.md)
 - [EdgeStatusDsLandevices](docs/EdgeStatusDsLandevices.md)
 - [EdgeStatusDsPathstats](docs/EdgeStatusDsPathstats.md)
 - [EdgeStatusDsPathstatsDspsPathstatsSample](docs/EdgeStatusDsPathstatsDspsPathstatsSample.md)
 - [EdgeStatusDsPathstatsDspsPs](docs/EdgeStatusDsPathstatsDspsPs.md)
 - [EdgeStatusDsResusage](docs/EdgeStatusDsResusage.md)
 - [EdgeStatusDsResusageDsrContainers](docs/EdgeStatusDsResusageDsrContainers.md)
 - [EdgeStatusDsResusageDsrLoadavg](docs/EdgeStatusDsResusageDsrLoadavg.md)
 - [EdgeStatusDsResusageDsrMemory](docs/EdgeStatusDsResusageDsrMemory.md)
 - [EdgeStatusDsResusageDsrNetwork](docs/EdgeStatusDsResusageDsrNetwork.md)
 - [EdgeStatusDsResusageDsrNetworkDsrnCellularStats](docs/EdgeStatusDsResusageDsrNetworkDsrnCellularStats.md)
 - [EdgeStatusDsResusageDsrNetworkDsrnIfGeolocation](docs/EdgeStatusDsResusageDsrNetworkDsrnIfGeolocation.md)
 - [EdgeStatusDsResusageDsrNetworkDsrnIfstats](docs/EdgeStatusDsResusageDsrNetworkDsrnIfstats.md)
 - [EdgeStatusDsResusageDsrNetworkDsrnTrafficstats](docs/EdgeStatusDsResusageDsrNetworkDsrnTrafficstats.md)
 - [EdgeStatusDsResusageDsrStorage](docs/EdgeStatusDsResusageDsrStorage.md)
 - [EdgeStatusDsUserinfo](docs/EdgeStatusDsUserinfo.md)
 - [EdgeStatusDsUserinfoDsuUsers](docs/EdgeStatusDsUserinfoDsuUsers.md)
 - [EdgeStatusRef](docs/EdgeStatusRef.md)
 - [EdgesList](docs/EdgesList.md)
 - [FirewallRule](docs/FirewallRule.md)
 - [GatewayDevicesAggregatedDeviceFlowStats](docs/GatewayDevicesAggregatedDeviceFlowStats.md)
 - [GatewayDevicesAggregatedDeviceFlowStatsData](docs/GatewayDevicesAggregatedDeviceFlowStatsData.md)
 - [GatewayDevicesAggregatedDeviceStats](docs/GatewayDevicesAggregatedDeviceStats.md)
 - [GatewayDevicesAggregatedDeviceStatsData](docs/GatewayDevicesAggregatedDeviceStatsData.md)
 - [GatewayInterfacesLatestStats](docs/GatewayInterfacesLatestStats.md)
 - [GatewayInterfacesLatestStatsCellularStats](docs/GatewayInterfacesLatestStatsCellularStats.md)
 - [GatewayInterfacesLatestStatsData](docs/GatewayInterfacesLatestStatsData.md)
 - [GatewayInterfacesLatestStatsWifiStats](docs/GatewayInterfacesLatestStatsWifiStats.md)
 - [GatewayPathsLatestStats](docs/GatewayPathsLatestStats.md)
 - [GatewayPathsLatestStatsData](docs/GatewayPathsLatestStatsData.md)
 - [GatewayRoutesLatestStats](docs/GatewayRoutesLatestStats.md)
 - [GatewayRoutesLatestStatsData](docs/GatewayRoutesLatestStatsData.md)
 - [GatewaySysLoadStats](docs/GatewaySysLoadStats.md)
 - [GatewaySysLoadStatsData](docs/GatewaySysLoadStatsData.md)
 - [GatewaySysLteSignalStats](docs/GatewaySysLteSignalStats.md)
 - [GatewaySysLteSignalStatsData](docs/GatewaySysLteSignalStatsData.md)
 - [GatewaySysMemoryStats](docs/GatewaySysMemoryStats.md)
 - [GatewaySysMemoryStatsData](docs/GatewaySysMemoryStatsData.md)
 - [GatewaySysUptimeStats](docs/GatewaySysUptimeStats.md)
 - [GatewaySysUptimeStatsData](docs/GatewaySysUptimeStatsData.md)
 - [GatewaySysWiFiStrengthStats](docs/GatewaySysWiFiStrengthStats.md)
 - [GatewaySysWiFiStrengthStatsData](docs/GatewaySysWiFiStrengthStatsData.md)
 - [GatewayWanAggregatedPathsAndLinksStats](docs/GatewayWanAggregatedPathsAndLinksStats.md)
 - [GatewayWanAggregatedPathsAndLinksStatsData](docs/GatewayWanAggregatedPathsAndLinksStatsData.md)
 - [GatewayWanPathsAndLinksStats](docs/GatewayWanPathsAndLinksStats.md)
 - [InboundNatRule](docs/InboundNatRule.md)
 - [InfiotErrorResponse](docs/InfiotErrorResponse.md)
 - [InterfaceSettings](docs/InterfaceSettings.md)
 - [InterfaceSettingsAddresses](docs/InterfaceSettingsAddresses.md)
 - [L4Protocols](docs/L4Protocols.md)
 - [LteInterfaceSetting](docs/LteInterfaceSetting.md)
 - [ManagedDevice](docs/ManagedDevice.md)
 - [ManagedDeviceList](docs/ManagedDeviceList.md)
 - [ManagedDevicePolicy](docs/ManagedDevicePolicy.md)
 - [ManagedDevicePolicyList](docs/ManagedDevicePolicyList.md)
 - [ManagedDevicePolicyService](docs/ManagedDevicePolicyService.md)
 - [ManagedDeviceProps](docs/ManagedDeviceProps.md)
 - [ManagedDeviceService](docs/ManagedDeviceService.md)
 - [MqttgcpConfiguration](docs/MqttgcpConfiguration.md)
 - [MqttgcpConfigurationTopic](docs/MqttgcpConfigurationTopic.md)
 - [NetflowCollector](docs/NetflowCollector.md)
 - [NetflowExporterSetting](docs/NetflowExporterSetting.md)
 - [ObjectProps](docs/ObjectProps.md)
 - [ObjectRef](docs/ObjectRef.md)
 - [OverlaySetting](docs/OverlaySetting.md)
 - [PagedResponse](docs/PagedResponse.md)
 - [Policy](docs/Policy.md)
 - [PolicyClassOfService](docs/PolicyClassOfService.md)
 - [PolicyConfig](docs/PolicyConfig.md)
 - [PolicyConfigPcfgFirewall](docs/PolicyConfigPcfgFirewall.md)
 - [PolicyConfigPcfgFirewallPcfgFwLogging](docs/PolicyConfigPcfgFirewallPcfgFwLogging.md)
 - [PolicyConfigPcfgGeneralSettings](docs/PolicyConfigPcfgGeneralSettings.md)
 - [PolicyConfigPcfgGeneralSettingsPcfgNetflow](docs/PolicyConfigPcfgGeneralSettingsPcfgNetflow.md)
 - [PolicyConfigPcfgUrlFilter](docs/PolicyConfigPcfgUrlFilter.md)
 - [PolicyFirewallAction](docs/PolicyFirewallAction.md)
 - [PolicyLinkSteeringAction](docs/PolicyLinkSteeringAction.md)
 - [PolicyLinkSteeringActionLnksVia](docs/PolicyLinkSteeringActionLnksVia.md)
 - [PolicyLinkSteeringActionLnksViaActive](docs/PolicyLinkSteeringActionLnksViaActive.md)
 - [PolicyLinkSteeringActionLnksViaBackup](docs/PolicyLinkSteeringActionLnksViaBackup.md)
 - [PolicyMatchRule](docs/PolicyMatchRule.md)
 - [PolicyPbrAction](docs/PolicyPbrAction.md)
 - [PolicyQoS](docs/PolicyQoS.md)
 - [PolicyQoSAction](docs/PolicyQoSAction.md)
 - [PolicyRef](docs/PolicyRef.md)
 - [PolicySchedulerAction](docs/PolicySchedulerAction.md)
 - [PolicyTrafficAction](docs/PolicyTrafficAction.md)
 - [PolicyTrafficPriority](docs/PolicyTrafficPriority.md)
 - [PolicyType](docs/PolicyType.md)
 - [ProxyArpSetting](docs/ProxyArpSetting.md)
 - [RadiusSetting](docs/RadiusSetting.md)
 - [SnmpSetting](docs/SnmpSetting.md)
 - [SnmpTrapSetting](docs/SnmpTrapSetting.md)
 - [StaticRoute](docs/StaticRoute.md)
 - [SyslogServer](docs/SyslogServer.md)
 - [Tenant](docs/Tenant.md)
 - [TenantTypeInput](docs/TenantTypeInput.md)
 - [TenantsList](docs/TenantsList.md)
 - [TimeSeriesProps](docs/TimeSeriesProps.md)
 - [TrafficMatchCriteria](docs/TrafficMatchCriteria.md)
 - [UpdateEdgeInput](docs/UpdateEdgeInput.md)
 - [User](docs/User.md)
 - [UserGroupRef](docs/UserGroupRef.md)
 - [UserRef](docs/UserRef.md)
 - [UserRole](docs/UserRole.md)
 - [Vrrp](docs/Vrrp.md)
 - [WebReputation](docs/WebReputation.md)
 - [WiFiInterfaceSetting](docs/WiFiInterfaceSetting.md)
 - [WiFiInterfaceSettingEncryption](docs/WiFiInterfaceSettingEncryption.md)

## Documentation For Authorization

## AuthToken

## Author



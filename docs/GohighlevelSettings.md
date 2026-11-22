# Zernio.Model.GohighlevelSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Platform** | **string** |  | 
**LocationId** | **string** | The HighLevel sub-account (location) id. | 
**CompanyId** | **string** | The agency that owns the sub-account, null for a sub-account under no agency. | 
**LocationName** | **string** |  | 
**InstalledBy** | **string** | The HighLevel user who installed the app. | 
**RelayConversions** | **bool** | CRM events are relayed as conversions. Default true. | 
**WriteBackAttribution** | **bool** | Relayed conversions are written back onto the HighLevel contact. Default true. | 
**ReportToAds** | **bool** | Relayed conversions are forwarded to the profile&#39;s ad platforms. A new connection starts with this on when its profile already sends events to an ad account, else off; reconnecting keeps the value. | 
**SyncContacts** | **bool** | Inbox contacts are matched to HighLevel contacts by phone, then email, and created there when none matches. Default true. | 
**LogMessages** | **bool** | Inbox messages from every channel (both directions) are logged on the HighLevel contact as one note per channel and day. Default true. | 
**LogDeliveryStatus** | **bool** | Logged outgoing messages show their delivery status (sent, delivered, read, failed) on their note line. Default true. | 
**SyncAdLeads** | **bool** | Leads from the profile&#39;s ad network lead forms become HighLevel contacts, deduplicated by email, then phone. Default true. | 
**MirrorConversations** | **bool** | Telegram, LINE, WeChat, iMessage and RCS messages go into the contact&#39;s Conversations thread under the Zernio channel (answerable from HighLevel) instead of a note. Default true. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


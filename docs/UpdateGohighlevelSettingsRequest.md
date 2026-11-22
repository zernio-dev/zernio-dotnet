# Zernio.Model.UpdateGohighlevelSettingsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RelayConversions** | **bool** | Relay HighLevel CRM events (new contacts, won opportunities, appointments, paid invoices and orders) as conversions with &#x60;source&#x60; &#x60;gohighlevel&#x60;. | [optional] 
**WriteBackAttribution** | **bool** | Write each relayed conversion onto the &#x60;Zernio Conversions&#x60; custom field of the HighLevel contact. | [optional] 
**ReportToAds** | **bool** | Also forward relayed conversions to the profile&#39;s ad platform destinations. Off stores them only. | [optional] 
**SyncContacts** | **bool** | Match inbox contacts to HighLevel contacts (phone, then email) and create the ones that do not exist. | [optional] 
**LogMessages** | **bool** | Log inbox messages from every channel on the matched HighLevel contact, one note per channel and UTC day. | [optional] 
**LogDeliveryStatus** | **bool** | Mark sent, delivered, read and failed on logged outgoing messages. | [optional] 
**SyncAdLeads** | **bool** | Create or update a HighLevel contact for every lead from the profile&#39;s ad network lead forms (Meta, TikTok, LinkedIn, Google), tagged with the network, campaign and form. | [optional] 
**MirrorConversations** | **bool** | Put Telegram, LINE, WeChat, iMessage and RCS messages into the contact&#39;s Conversations thread under the Zernio channel, so a HighLevel user reads and answers them there. Off logs them as notes. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


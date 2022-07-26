# Change in Automation API access token scope

**Date Announced**

27 July 2022

**Effective Date**

27 July 2022

**Change behaviour**

This change is backward compatible for two months from 27 July 2022. Later, we will update you with the date when this change becomes a non-breaking change.

**Details**

There is a new change to the `scope` parameter in the request for access token via client credentials grant. You are required to change the `scope` parameter value from `https://graph.microsoft.com/.default` to `https://api.techpass.gov.sg/.default`

**Why was this changed?**

The **aud** claim in an access token indicates the resource token is intended for its audience. The `scope` parameter in the request for access token defines this value. For more information, refer to [Microsoft documentation](https://docs.microsoft.com/en-us/azure/active-directory/develop/access-tokens).

In the context of TechPass Automation API, the token that we receive from our callers(tenant applications) should have the **aud** claim pointing to us since we are the intended audience of the token. However, we have been accepting access tokens with **aud** claim pointing to Microsoft Graph `https://graph.microsoft.com`.

With the **aud** claim pointing to Microsoft Graph, the responsibility to validate the access token lies with Microsoft, and we have no way to validate the signature of the token as Microsoft uses a special signing-in in mechanism that only they know how to validate. For more information, refer to the [issue](https://github.com/AzureAD/azure-activedirectory-identitymodel-extensions-for-dotnet/issues/609#issuecomment-524434987).

The new change would not only allow us to validate the **signature** of the token using public validators but also helps us to ensure that the token is for TechPass Automation API by matching the **aud** claim against the TechPass Automation API endpoint.

**Action required**

Change the `scope` parameter value from `https://graph.microsoft.com/.default` to `https://api.techpass.gov.sg/.default` in the request for access token via client credentials grant.

This change returns `https://api.techpass.gov.sg` as the **aud** claim of the access token. Your API has to validate this **aud** value and also the **signature** of the access token. For more information, refer to [Validating Access Token](https://stg.docs.developer.tech.gov.sg/docs/techpass-tenant-guide/#/apis/integration?id=validating-access-token).


**How does this impact tenant applications?**

This change will be backward compatible(non-breaking change) for two months from 27th July 2022. We will update you later when it nears the end of the backward compatibility. When it becomes a non-backward compatible (breaking change) only `https://api.techpass.gov.sg/.default` will be accepted.

After two months, if the access token **aud** claim does not point to `https://api.techpass.gov.sg`, tenant applications making calls to TechPass Automation API will receive an error.

.. _refApiResource:
API Resource
=================
This class model an API resource.

``Enabled``
    Indicates if this resource is enabled and can be requested. Defaults to true.
``Name``
    The unique name of the API. This value is used for authentication with introspection and will be added to the audience of the outgoing access token.
``DisplayName``
    This value can be used e.g. on the consent screen.
``Description``
    This value can be used e.g. on the consent screen.
``ApiSecrets``
    The API secret is used for the introspection endpoint. The API can authenticate with introspection using the API name and secret.
``UserClaims``
    List of associated user claim types that should be included in the access token.
``Scopes``
    An API must have at least one scope. Each scope can have different settings.


Scopes
^^^^^^
In the simple case an API has exactly one scope. But there are cases where you might want to sub-divide the functionality of an API, 
and give different clients access to different parts.

``Name``
    The unique name of the scope. This is the value a client will use for the scope parameter in the authorize/token request.
``DisplayName``
    This value can be used e.g. on the consent screen.
``Description``
    This value can be used e.g. on the consent screen.
``Required``
    Specifies whether the user can de-select the scope on the consent screen (if the consent screen wants to implement such a feature). Defaults to false.
``Emphasize``
    Specifies whether the consent screen will emphasize this scope (if the consent screen wants to implement such a feature). Use this setting for sensitive or important scopes. Defaults to false.
``ShowInDiscoveryDocument``
    Specifies whether this scope is shown in the discovery document. Defaults to true.
``UserClaims``
    List of associated user claim types that should be included in the access token. The claims specified here will be added to the list of claims specified for the API.

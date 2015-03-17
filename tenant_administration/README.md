# Tenant Administration
Messaging tenants are tied to CCA organizations right now, so only one tenant can be created for each company, unless they create divisions to host additional tenants. Two trading partners are created so that senders cannot see all of receiver’s messages. A HTTP mailbox for each trading partner is created while creating Teant.

Teannt is created in hte sytem by Message Administrator and this will be handled through database scripts at this time. A request to create a Tenant is handle outside the messaging application. (Via CRT).

Messagiong Administrator can delete Tenant and it is and handle through database. Must physically delete all trading partner messages, all trading partner rules, all trading partner channels, all trading partners for tenant and role grants for tenant before physically deleting tenant entity.


# Kerberos Schema

Event fields used to define Kerberos Ticket Granting Service and Kerberos Ticket Granting Tickets.  
For certificate information within Kerberos see the [X509 and Certificates Schema](./x509_and_certificates.md)

## Data Fields

| Standard Name | Type | Description | Sample Value |
|--------|---------|-------|-------|
|service_name|string|the name of the account or computer for which the TGS ticket was requested|WIN2008R2$|
|ticket_options|string|this is a set of different ticket flags in hexadecimal format.|0x40810010|
|ticket_status|string|hexadecimal result code of TGS issue operation.|0x0|
|ticket_encryption_type|string|the cryptographic suite that was used for issued TGS.|0x12|
|ticket_request_type|string|Request type - Authentication Service (“AS”) or Ticket Granting Service (“TGS”)|TGS|
|service_name|string|the name of the service in the Kerberos Realm to which TGT request was sent. Typically has value "krbtgt" for TGT requests, which means Ticket Granting Ticket issuing service. For Failure events Service Name typically has the following format: krbtgt/REALM_NAME. For example: krbtgt/CONTOSO.|krbtgt|
|ticket_options|string|this is a set of different ticket flags in hexadecimal format.|0x40810010|
|ticket_status|string|hexadecimal result code of TGT issue operation.|0x0|
|ticket_encryption_type|string|the cryptographic suite that was used for issued TGT|0x12|
|ticket_pre_auth_type|integer|the code number of pre-Authentication type which was used in TGT request.|15|
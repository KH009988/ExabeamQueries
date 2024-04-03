_NOTE: Some of these fields that are being used may be different in your environment depending on parsing._ 

### Root User Login: 
`(Product:"AWS CloudTrail" AND event_name:"ConsoleLogin") AND user_identity:"root"`

### IF user identity field is not parsed & Regex is needed: 
`(Product:"AWS CloudTrail" AND event_name:"ConsoleLogin") AND RGXi("userIdentity\"\:\{\"type\"\:\"root")`

Inspiration/Reference: https://www.elastic.co/guide/en/security/current/aws-management-console-root-login.html, https://docs.aws.amazon.com/signin/latest/userguide/account-root-user-type.html

# Simulating Risk Detections
Leaked Credentials for Workload Identities and Users

# Simulate Leaked Credentials in GitHub for Workload Identities

    - Sign in to the Microsoft Entra admin center as at least a Security Administrator.
    - Browse to Identity > Applications > App registrations.
    - Select New registration to register a new application or reuse an existing stale application.
    - Select Certificates & Secrets > New client Secret , add a description of your client secret and set an expiration for the secret or specify a custom lifetime and select Add. Record the secret's value for later use for your GitHub Commit.
    - Get the TenantID and Application(Client)ID in the Overview page.

  # Ensure you disable the application via Identity > Applications > Enterprise Application > Properties > Set Enabled for users to sign-in to No.

    - Create a public GitHub Repository, add the following config and commit the change as a file with the .txt extension.


#File:

  "AadClientId": "XXXX-2dd4-4645-98c2-960cf76a4357",
  "AadSecret": "p3n7Q~XXXX",
  "AadTenantDomain": "XXXX.onmicrosoft.com",
  "AadTenantId": "99d4947b-XXX-XXXX-9ace-abceab54bcd4",

In about 8 hours, you'll be able to view a leaked credential detection under Protection > Identity Protection > Risk Detection > Workload identity detections where the additional info will contain the URL of your GitHub commit.

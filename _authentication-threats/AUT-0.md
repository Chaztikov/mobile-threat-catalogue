---
    layout: threat
    ThreatCategory: "Authentication: User or Device to Remote Service"
    ID: AUT-0
    Threat: "Theft (Use of authorized credentials)"
    ThreatOrigin: "Mobile Threat Protection: A Holistic Approach to Securing Mobile Data and Devices [^61]"
    ExploitExample:
        - "CBS App & Mobility Website [^116]"
        - "The Fork [^117]"
        - "Star Q8 [^118]"
        - "Corriere Della Sera App [^119]"
        - "LaTribune [^120]"
        - "Card Crypt [^121]"
        - "Starbucks Caught Storing Mobile Passwords in Clear Text [^122]"
    CVEExample:
    PossibleCountermeasures:
        "Use anomaly detection based on user activity to detect abnormal actions (e.g. authentication from new domains, unusual times, or to rarely-accessed services) and require additional authentication steps before granting access.":
            - Enterprise
        "When possible, configure services to use multi-factor authentication. Ideally, the additional factor should be provided by a separate device than the one being used to perform primary authentication (e.g., laptop and mobile app). Further, avoid the use of SMS messages for 2FA codes, as SMS messages can be readily intercepted.":
            - Mobile Device User
            - Enterprise
        "Use centralized identity and access management tools that permit simultaneous revocation of stolen authentication credentials across all access control mechanisms and terminate active sessions based on those credentials.":
            - Enterprise
        "To minimize the value of stolen credentials, enforce a policy that limits the maximum age of credentials and limits the use of identical or similar credentials.":
            - Enterprise
        "Enforce an access policy that restricts the resources a user can access based on location parameters (e.g. domain, IP address, MAC address, geolocation) of the authentication request. Incorporate the principle of least privilege to limit lateral movement by an attacker with stolen credentials.":
            - Enterprise
        "Employ authentication mechanisms that utilizes randomly generated one-time passwords or tokens for access from untrusted locations. If stolen, (at worst) this would only grant an attacker temporary access. This should be combined with stronger authentication mechanisms being required for a user to change authentication credentials or obtain additional one-time passwords.":
            - Enterprise
---

# Phishing Incident Response Checklist

## Initial Validation
- Identify affected user
- Confirm alert source
- Review email subject and sender

## Email Analysis
- Check sender domain reputation
- Analyze URLs and attachments
- Look for spoofing indicators

## User Activity Review
- Confirm if link was clicked
- Review Azure AD sign-in logs
- Check for abnormal login locations

## Endpoint Investigation
- Review EDR alerts
- Check for malware or PowerShell execution
- Analyze suspicious processes

## Containment
- Block malicious URLs/domains
- Reset user credentials if required
- Isolate endpoint if compromised

## Documentation
- Capture IOCs (IP, domain, URL, hash)
- Document findings and actions taken

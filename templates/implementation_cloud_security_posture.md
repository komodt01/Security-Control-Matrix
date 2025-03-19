# Cloud Security Posture Management Template
*Sources: CSA Cloud Controls Matrix v4.0, CIS Benchmarks 2024*

## Configuration Baseline

### AWS Security Configuration
```json
{
    "securityhub": {
        "standards": {
            "cis": "enabled",
            "pci": "enabled",
            "iso": "enabled"
        },
        "automated_response": {
            "severity": "HIGH",
            "actions": ["isolate", "notify"]
        }
    },
    "guardduty": {
        "enabled": true,
        "findings_notification": {
            "threshold": "MEDIUM",
            "sns_topic": "arn:aws:sns..."
        }
    }
}
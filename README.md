# Project 17: Log Forwarding to CloudWatch

## Goal
Central log management with Amazon CloudWatch Logs.

## What was done
1. Installed the Amazon CloudWatch Agent on the Ubuntu VM (on-premises mode).
2. Configured it to forward Apache access/error logs and syslog
   to log group aijaz-p17-logs (7-day retention), one stream per file.
3. Generated web traffic (200 and 404 responses).
4. Verified logs and summarised HTTP status codes with a Logs Insights query (CLI).

## Result
- Agent status: running
- Log streams: apache-access, apache-error, syslog
- Logs Insights summary: 80 x HTTP 200, 81 x HTTP 404

## Files
- amazon-cloudwatch-agent.json: agent configuration
- dashboard.json: CloudWatch dashboard definition

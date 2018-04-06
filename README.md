# Example Fluentd (Td-agent) configuration file

### Prerequisities:
- Fluentd v1.0.2 (td-agent 3.1.1-0)
- AWS credentials to upload file on S3 bucket

### Command line:
- Start Td-agent service:

		$ sudo /etc/init.d/td-agent start
	
- Stop Td-agent service:

		$ sudo /etc/init.d/td-agent stop
	
- Restart Td-agent service:

		$ sudo /etc/init.d/td-agent restart
	
- Td-agent configuration file (nano or vi editor):
	
		$ sudo nano /etc/td-agent/td-agent.conf
	
- Td-agent log file:

		$ tail -100 /var/log/td-agent/td-agent.log
		
### Original file row example:
2018-04-06 12:00:00,000|STREAM-LIN|0|username0|123|field1|field2|field3|||||field...|||||||||it|fieldN

### Td-agent result file:
2018-04-06 12:00:00|CET|123|TEST|it

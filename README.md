Python Honeypot

Overview

This project is a simple SSH honeypot built in Python. It simulates an SSH service to attract and log unauthorized access attempts, helping to study attacker behavior and analyze potential threats.

Features

	•	Simulates an SSH service on a configurable port.
	•	Captures and logs connection attempts, including IP addresses and interaction data.
	•	Can be extended with additional features like fake commands or real-time alerts.

Usage

Prerequisites

	•	Python 3.x installed on a Linux system (tested on Kali Linux).
	•	Root privileges (required to bind to ports below 1024).

Installation

	1.	Clone or download this repository.
	2.	Navigate to the project folder.

Run the Honeypot

	1.	Open a terminal and run:

sudo python3 honeypot.py


	2.	The honeypot will start listening on the default port (2222).

Test the Honeypot

You can test it using an SSH client:

ssh -p 2222 127.0.0.1

Logs

All activity is logged in the honeypot.log file in the project directory. Example log output:

[2024-11-16 12:34:56] Connection from 192.168.1.10
Data Received: ssh user@192.168.1.10
--------------------------------------------------

Customization

Change the Listening Port

Edit the PORT variable in the script to any desired port number:

PORT = 3333

Simulate More SSH Responses

Modify the client_socket.send line to include more realistic or custom responses.

Add Real-Time Alerts

Integrate email or chat notifications using services like Telegram or Twilio for instant alerts.

Future Improvements

	•	Implement a fake shell for attackers to interact with.
	•	Capture and analyze brute-force password attempts.
	•	Visualize attack data with tools like Grafana or Kibana.
	•	Deploy the honeypot on a public cloud for real-world testing (with caution).

Disclaimer

This project is for educational and research purposes only. Do not use it for unauthorized surveillance or illegal activities. Deploy responsibly and ensure compliance with local laws.

Author

Developed by Ani Chigozie Destiny as part of a cybersecurity learning project.

Visit my GitHub for more projects

Feel free to tweak it to your needs or add any additional features you might implement later!
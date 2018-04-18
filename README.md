# Server Remote Console (SA-MP)

This web application wrote in PHP is a simple remote console to manage players and server activities.
You can easily start & stop your server, once configured, and you can view server logs as well as server advanced informations and player's list. Moreover, it is possible to kick or ban players directely from the console and send global messages.

## Features

- Easy configuration
- No mysql database needed
- Multiple types of configuration based on needs
- Password protected area
- Simple Server Start (via SSH)
- Simple Server Stop (via RCON)
- Possibility to send global message to ingame players (via RCON)
- Direct access to server_logs.txt and quick reset (via SSH)
- Advanced information panel about the server
- Advanced player's list (with score, username, id and ping)
- Bootstrap 4.0 coding and font-awesome icons


## Requirements

- 1) Web server with PHP 7.0+ (it should work fine in PHP 5)
- 2) [Recommended] SA-MP server on Ubuntu or Debian
- 3) [Recommended] RCON password of the server
- 4) [Recommended] SSH access to samp-server directory with granted privileges 


## Installation

The installation process is pretty easy: you need to edit the file ```includes/configuration.php``` with the requested field. In order to make everything usable, you must have satisfy all the recommended requirements described above. Anyway, there are various modes to use this console.

Modes | Description | Requirements
---   | ---         | ---
**Open Mode** | This mode is used to display only the server information and player's list. Guests are able to see this everything and nothing else. | (1)
**Limited Mode** | In this mode, you need a password to access the area and you can only view server information and player's list. | (1)
**Only RCON Mode** | Like the limited mode, but with the possibility to kick and ban players, stop server and send global messages. | (1) (3)
**Only SSH Mode** | Like the limited mode, with the possibility to start the server, view and reset server_logs. | (1) (2) (4)
**Complete Mode** | All the features. | (1) (2) (3) (4)



## Configuration File

	   	
- **EnableRCON** activates the following features:
	- Kick / Ban players
	- Message
	- Stop server
 	- [Requirement:] YOU NEED A SSH ACCESS WITH SA-MP FOLDER PERMISSIONS		
	 

- **EnableSSH** activates the following features:
 	- View / Reset server logs
	- Start server
	- [Requirement:] YOU NEED SSH ACCESS WITH SA-MP FOLDER PERMISSIONS TO ENABLE THIS FEATURE		

- **EnableSRCPassword** is used to enable / disable password protected area for this console.
   		[IMPORTANT] 
   			It is strongly recommended to use it only if BOTH EnableSSH and EnableRCON are disabled, because it activates remote control to guests.





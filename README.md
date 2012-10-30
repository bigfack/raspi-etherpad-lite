<html>
<head>
</head>
	<body>
		<h2>Summary</h2>
		This script is intended to install Etherpad-Lite on to a Raspberry Pi running Raspian/Raspbian. It relies on bash, access to internet, and root privileges.
		<h2>What it Does</h2>
		<ul>
			<li>Checks to make sure it's being run with root privileges
			<li>Uses variables with which user can customize a little
			<li>Uses package manager to download dependencies.
			<li>Uses git clone to download source to target directory
			<li>Creatings settings file from template and configures for basic use (no mysql, for example)
			<li>Checks for npm and node dependencies and downloads as necessary
			<li>Creates a system user and a group named etherpad-lite and grants permissions as necessary
			<li>Sets up daemon to start server at start up.
		</ul>
		<h2>Usage</h2>
		<ol>
			<li>Download the script. It's available here on github using git. You'll need git later, so: sudo apt-get install git. Then use git clone git://github.com/ghoulmann/NAME.git. Or you can download and then unzip Name of file.zip.
			<li>Edit install_raspi_etherpad-lite with the text editor you're most comfortable with. Nano, leafpad, vi, emacs will all do. e.g. nano ./install_raspi_etherpad-lite. Edit the values for the port and the target directory: the defaults work, but the flexibility is there if you want it.
			<li>Run the script with root privileges. It should already be executeable. If not, sudo chmod +x ./install_raspi_etherpad-lite . Then do sudo ./install_raspi_etherpad-lite .
		</ol>
<p>The etherpad-lite service should start automatically next time you boot. If, however, you'd like to start it immediately, do sudo service etherpad-lite start.
	</body>
</html>
WhatsApp Desktop for Linux
This is the WhatsApp Desktop application for Linux, allowing you to run WhatsApp on your Ubuntu (or other Linux distributions) without using a web browser.

📦 What’s Included:
WhatsApp-linux-x64: The portable executable version of WhatsApp.

Icon: The WhatsApp icon to integrate the app seamlessly into your desktop environment.

Configuration Files: All necessary files to run WhatsApp on your system, including resources and dependencies.

🚀 Features:
Native WhatsApp experience on Linux.

Standalone app with no need for a browser.

Integration with your desktop environment, just like any other native application.

🔧 Installation Instructions:
Download the WhatsApp-linux-x64 Release:

Navigate to the Releases section on the GitHub page and download the WhatsApp-linux-x64 release.

Extract the Files:

Extract the downloaded files to a folder of your choice (e.g., /home/<your-username>/Apps/WhatsApp-linux-x64/).

Create a Desktop Entry:

Open a terminal and create a new desktop entry file:

bash
Copy
Edit
nano ~/.local/share/applications/whatsapp.desktop
Paste the following content into the file, replacing <your-username> with your actual username and adjusting paths if necessary:

ini
Copy
Edit
[Desktop Entry]
Name=WhatsApp
Exec=/home/<your-username>/Apps/WhatsApp-linux-x64/WhatsApp
Icon=/home/<your-username>/Apps/WhatsApp-linux-x64/resources/app/icon.png
Type=Application
Categories=Network;InstantMessaging;
StartupWMClass=WhatsApp
Terminal=false
Save and close the file.

Make the Desktop Entry Executable:

In the terminal, run:

bash
Copy
Edit
chmod +x ~/.local/share/applications/whatsapp.desktop
Refresh the Desktop Database (Optional):

You can refresh the desktop database to make sure everything is up to date by running:

bash
Copy
Edit
update-desktop-database ~/.local/share/applications
Launch WhatsApp:

You can now search for WhatsApp in your application menu and launch it like any other app.

⚙️ Requirements:
Ubuntu 18.04 or later (or any Linux distribution with similar package management).

A graphical user interface (GUI) for running the application.

📝 Known Issues:
WhatsApp may not show up in some desktop environments after installation. If that happens, refer to the installation troubleshooting section below.

🔄 Future Releases:
v2.0 will include improvements, bug fixes, and new features such as support for multiple WhatsApp accounts.

🚨 Important Notes:
This is an unofficial, portable release of WhatsApp for Linux.

Make sure to update the application to the latest release for security and feature updates.

🖼️ Troubleshooting:
App not launching?

Ensure that the path in the Exec line of the whatsapp.desktop file is correct and points to the WhatsApp executable.

Icon not visible?

Ensure the icon path exists and is a valid .png file. You can try replacing the icon with another valid image if needed.

Permission Denied?

Make sure the WhatsApp binary itself is also executable:

bash
Copy
Edit
chmod +x /home/<your-username>/Apps/WhatsApp-linux-x64/WhatsApp
❓ How to Uninstall:
To remove WhatsApp from your system:

Delete the desktop entry:

bash
Copy
Edit
rm ~/.local/share/applications/whatsapp.desktop
Delete the WhatsApp folder where you extracted the files, e.g., /home/<your-username>/Apps/WhatsApp-linux-x64/.

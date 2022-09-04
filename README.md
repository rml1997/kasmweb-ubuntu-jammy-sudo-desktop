# kasmweb-ubuntu-jammy-sudo-desktop
Prerequisites:

Install Kasmweb by following https://kasmweb.com/docs/latest/install/single_server_install.html

Login with a user with admin access

I used Oracle cloud as this runs in their free forever tier with a pretty powerful arm machine

Once this is setup and you can connect to the Ubuntu Jammy image, you're ready

Add sudo to the kasmweb ubuntu jammy desktop image:

SSH onto Kasm Agent

nano Dockerfile

Paste the contents of Dockerfile from this repo

sudo docker build -t ubuntu-jammy-sudo-desktop:1.11.0 -f Dockerfile .

Go to Admin -> Images

Ubuntu Jammy -> ... -> Clone

Change Docker Image to kasmweb/ubuntu-jammy-sudo-desktop:1.11.0

Change Friendly name to Ubuntu Jammy with sudo

Delete Docker Registry entry

Click Submit

That's it!

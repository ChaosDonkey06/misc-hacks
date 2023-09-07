# Install Dropbox Server
Courtesy of Felipe González-Casabianca

**Last used on 2021**

# Download
cd ~ && wget -O - "https://www.dropbox.com/download?plat=lnx.x86_64" | tar xzf -

# If dropbox has a lot of files
echo fs.inotify.max_user_watches=1000000

sudo tee -a /etc/sysctl.conf; sudo sysctl -p

# Probably missing packages

<div class="list">

sudo apt-get install -y libglapi-mesa

sudo apt-get install -y libxdamage-dev

sudo apt-get install -y libxcb-glx0

sudo apt-get install libxcb-dri2-0

sudo apt-get install -y libxcb-dri3-0

sudo apt-get install -y libxcb-present-dev

sudo apt-get install -y libxshmfence-dev

sudo apt-get install -y libxxf86vm-dev

</div>


# Install Deamon
~/.dropbox-dist/dropboxd

# Install CLI (must have python)

<div class="list">

sudo wget -O /usr/local/bin/dropbox "https://www.dropbox.com/download?dl=packages/dropbox.py"

sudo chmod +x /usr/local/bin/dropbox

</div>

# Exclude a lot of files
Command to exclude files/folders from synchronizing.

<div class="list">

dropbox exclude add <path_to_exclude>

</div>

# fire-tv-remote-desktop
How to tunnel a Fire TV Stick so that you can use the remote app from another network.

# Router setup

You're home router must be able to act as a VPN server. For example, on a Netgear Orbi, go to Advanced tab -> Advanced Setup -> VPN Service. Enable VPN Service. Note that if your IP address is not static from your ISP (which is likely the case), then you must setup up Dynamic DNS from a service like https://www.noip.com/.

Once Dynamic DNS and VPN service is enabled, download the OpenVPN configuration file. Choose "FOR SMART PHONE" to get the VPN configuration options as a zipped `.opvn` file.

Unzip the `.opvn` file and transfer it to the Fire Stick's memory. An easy way to transfer it is to uploaded it to Google Drive (or other cloud service), generate a shareable link, and used a URL shortener to download it to the Fire Stick with the [Downloader app](https://www.amazon.com/AFTVnews-com-Downloader/dp/B01N0BP507)

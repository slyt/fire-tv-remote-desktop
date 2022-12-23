# fire-tv-remote-desktop
How to tunnel a Fire TV Stick so that you can use the remote app from another network.

# Router setup

You're home router must be able to act as a VPN server. For example, on a Netgear Orbi, go to Advanced tab -> Advanced Setup -> VPN Service. Enable VPN Service. Note that if your IP address is not static from your ISP (which is likely the case), then you must setup up Dynamic DNS from a service like https://www.noip.com/.

Once Dynamic DNS and VPN service is enabled, download the OpenVPN configuration file. Choose "FOR SMART PHONE" to get the VPN configuration options as a zipped `.opvn` file.

Unzip the `.opvn` file and transfer it to the Fire Stick's memory. An easy way to transfer it is to uploaded it to Google Drive (or other cloud service), generate a shareable link, and used a URL shortener to download it to the Fire Stick with the [Downloader app](https://www.amazon.com/AFTVnews-com-Downloader/dp/B01N0BP507)

Next you'll need to install OpenVPN. Since OpenVPN is not available on the Fire Stick app store, you'll need to download the APK and install manually. Installing APK's manually requires developer settings to be enabled on the Fire Stick.

I used the OpenVPN apk from: [https://openvpn-connect.en.uptodown.com/android](https://openvpn-connect.en.uptodown.com/android/download).

Once OpenVPN is installed, you can import the `.opvn` config file to setup the VPN profile. I recommend going into the OpenVPN settings and selecting "Reconnect on Reboot". I notce that putting the Fire Stick to sleep kept the VPN connection alive, however doing a full restart caused the VPN to break, in which case you can just re-enable the connection in the OpenVPN app.

In order to control the Fire Stick remotely, you can use a remote desktop viewer like https://www.vysor.io/. With the VPN connection activiated, use the IP address of the VPN client in the Vysor desktop app.

It is also possible to use the native Fire Stick app to remotely control a Fire Stick over VPN, however, since there is no view of the screen, it is not very useful.

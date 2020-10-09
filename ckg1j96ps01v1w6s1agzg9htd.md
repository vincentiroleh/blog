## Create Bootable USB Media in Ubuntu Using BalenaEtcher

<span class="s"></span>

# Create Bootable USB Media in Ubuntu Using BalenaEtcher

Coming from Windows, RUFUS application has been the hot chick in town when it comes to creating a bootable USB. But RUFUS only supports Windows and Mac.

So if you are using Linux distributions, RUFUS is not the way to go. But fear not. Just as the case with almost every other task, popular Linux distros such as Ubuntu has never failed to meet the user demands. The same is the situation when you need to convert ISO to bootable USB Media in Ubuntu, Linux Mint, or any Debian distros.

In this tutorial, I’m going to show you how to create a bootable USB Media in Ubuntu within a minute. So I assume you already have Ubuntu running on your PC.

For this tutorial, I will be making an Ubuntu ISO 18.04 bootable in a USB 4GB flash drive.

**STEP 1: Downloading** [**Balena Etcher**](https://www.balena.io/etcher/) **Desktop App**

Open the terminal… **_Ctrl+Alt+T_**

*   Add Etcher debian repository:
    **_Press the Enter keyboard after every command._**

![Image for post](https://miro.medium.com/max/60/1*s0ya1ewSsaupzOeN1GU8cA.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/2732/1*s0ya1ewSsaupzOeN1GU8cA.png" width="1366" height="768" srcSet="https://miro.medium.com/max/552/1*s0ya1ewSsaupzOeN1GU8cA.png 276w, https://miro.medium.com/max/1104/1*s0ya1ewSsaupzOeN1GU8cA.png 552w, https://miro.medium.com/max/1280/1*s0ya1ewSsaupzOeN1GU8cA.png 640w, https://miro.medium.com/max/1400/1*s0ya1ewSsaupzOeN1GU8cA.png 700w" sizes="700px"/></noscript>


```
echo "deb [https://deb.etcher.io](https://deb.etcher.io) stable etcher" | sudo tee /etc/apt/sources.list.d/balena-etcher.list</span>
```


*   Trust Bintray.com’s GPG key:

![Image for post](https://miro.medium.com/max/60/1*ltKbb212dAWT_8lZmsiRpw.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/2732/1*ltKbb212dAWT_8lZmsiRpw.png" width="1366" height="768" srcSet="https://miro.medium.com/max/552/1*ltKbb212dAWT_8lZmsiRpw.png 276w, https://miro.medium.com/max/1104/1*ltKbb212dAWT_8lZmsiRpw.png 552w, https://miro.medium.com/max/1280/1*ltKbb212dAWT_8lZmsiRpw.png 640w, https://miro.medium.com/max/1400/1*ltKbb212dAWT_8lZmsiRpw.png 700w" sizes="700px"/></noscript>


```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 379CE192D401AB61</span>
```


*   Update and install:


```
sudo apt-get install balena-etcher-electron</span>
```


**Ever feel like uninstalling it?**
Uninstall:


```
sudo apt-get update</span>
```


**STEP 2: Open BalenaEtcher**

Search BalenaEtcher from your Application Menu, or simply press the Windows key and type ‘BalenaEtcher’.

![Image for post](https://miro.medium.com/max/60/1*-DFWS5k1miXHSwka6fdeTQ.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/2732/1*-DFWS5k1miXHSwka6fdeTQ.png" width="1366" height="768" srcSet="https://miro.medium.com/max/552/1*-DFWS5k1miXHSwka6fdeTQ.png 276w, https://miro.medium.com/max/1104/1*-DFWS5k1miXHSwka6fdeTQ.png 552w, https://miro.medium.com/max/1280/1*-DFWS5k1miXHSwka6fdeTQ.png 640w, https://miro.medium.com/max/1400/1*-DFWS5k1miXHSwka6fdeTQ.png 700w" sizes="700px"/></noscript>

Search for BalenaEtcher on ubuntu 18.04

**STEP 3: The Final Step (Making the USB Bootable)**

![Image for post](https://miro.medium.com/max/60/1*XSqALcgXE7RNhbjjahNQkw.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/1594/1*XSqALcgXE7RNhbjjahNQkw.png" width="797" height="508" srcSet="https://miro.medium.com/max/552/1*XSqALcgXE7RNhbjjahNQkw.png 276w, https://miro.medium.com/max/1104/1*XSqALcgXE7RNhbjjahNQkw.png 552w, https://miro.medium.com/max/1280/1*XSqALcgXE7RNhbjjahNQkw.png 640w, https://miro.medium.com/max/1400/1*XSqALcgXE7RNhbjjahNQkw.png 700w" sizes="700px"/></noscript>

balenaEtcher environment

The environment is simple and straight forward:

*   Select the image (iso file)
*   Select the flash drive plugged in the PC
*   Click on the Flash button, wait for the magic to happen

**Grab a cup of coffee, while the magic happens…**

![Image for post](https://miro.medium.com/max/60/1*bwlkpGzGiw7FGq5oG1x4Lw.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/1600/1*bwlkpGzGiw7FGq5oG1x4Lw.png" width="800" height="510" srcSet="https://miro.medium.com/max/552/1*bwlkpGzGiw7FGq5oG1x4Lw.png 276w, https://miro.medium.com/max/1104/1*bwlkpGzGiw7FGq5oG1x4Lw.png 552w, https://miro.medium.com/max/1280/1*bwlkpGzGiw7FGq5oG1x4Lw.png 640w, https://miro.medium.com/max/1400/1*bwlkpGzGiw7FGq5oG1x4Lw.png 700w" sizes="700px"/></noscript>

flashing<span class="io dp et ip iq ir"></span><span class="io dp et ip iq ir"></span><span class="io dp et ip iq"></span>![Image for post](https://miro.medium.com/max/60/1*KF7wiCCzEOaLJOCJwDTd-A.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/1600/1*KF7wiCCzEOaLJOCJwDTd-A.png" width="800" height="510" srcSet="https://miro.medium.com/max/552/1*KF7wiCCzEOaLJOCJwDTd-A.png 276w, https://miro.medium.com/max/1104/1*KF7wiCCzEOaLJOCJwDTd-A.png 552w, https://miro.medium.com/max/1280/1*KF7wiCCzEOaLJOCJwDTd-A.png 640w, https://miro.medium.com/max/1400/1*KF7wiCCzEOaLJOCJwDTd-A.png 700w" sizes="700px"/></noscript>

validating<span class="io dp et ip iq ir"></span><span class="io dp et ip iq ir"></span><span class="io dp et ip iq"></span>

**Boom!!! Magic Done.
Your USB flash drive is bootable, unmount your drive, and go make yourself proud…**

![Image for post](https://miro.medium.com/max/60/1*KVSuTR0yXUyO4s6qav4sBA.png?q=20)

<noscript><img alt="Image for post" class="t u v fu aj" src="https://miro.medium.com/max/1600/1*KVSuTR0yXUyO4s6qav4sBA.png" width="800" height="510" srcSet="https://miro.medium.com/max/552/1*KVSuTR0yXUyO4s6qav4sBA.png 276w, https://miro.medium.com/max/1104/1*KVSuTR0yXUyO4s6qav4sBA.png 552w, https://miro.medium.com/max/1280/1*KVSuTR0yXUyO4s6qav4sBA.png 640w, https://miro.medium.com/max/1400/1*KVSuTR0yXUyO4s6qav4sBA.png 700w" sizes="700px"/></noscript>

Flash complete


```
sudo umount /dev/sdc1</span>
```


Was this tutorial helpful?

*   **Clap**
*   Follow on [**Twitter**](https://twitter.com/IrolehVincent)
*   Come back for more cool stuff on **Web** && **Linux**
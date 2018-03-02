# BroadLink RM Bridge SmartThings Device Handler

## Requirements
A SmartThings hub and a Broadlink RM hub

A SmartThings developers account https://developers.smartthings.com/

An Android device with:
* The Rm Bridge Pro app
* The Broadlink E-Control app. This is only to get the MAC address of your device

## Setup
In your SmartThings developers account select you location in the My Locations tab.

Once done got the My Device Handlers tab and select Create New Device Handler in the top right.

Within this page select the From Code tab and paste in the code from device_handler.groovy and select `Publish > For Me`

Goto the My Devices tab at the top and hit New Device in the top right.

Give your new device a name (TV)

Give it a label if you want (My TV)

For the Device Network Id, give it a unique ID (LIVINGROOMTV)

In the Type dropdown scroll to the bottom and select Broadlink RM Pro Bridge which is the device handler we just created

Select your Location and Hub and hit Create

That's it for the developers section, hop back to your android device and open your SmartThings app.

Goto My Home and add a new device, your new device should now appear in the list of devices found.

Hit save and find your new device in the list of things. Select it and then hit the settings button in the top right.

In here you'll need to enter the hostname of your device which is the IP address shown in the RM Bridge app including the port number, which will look something like

`192.168.1.23:4567`

And you'll also need to enter the MAC address of your Broadlink device which can be found in the Broadlink E-Control app by hitting the plus sign in the top right and selecting device list from the dropdown. The MAC address is the code shown below the device name which will look something like

`12:ab:34:c5:d6:78`

And that's it...

# Usage
Select Learn to teach your device a new IR code, the orange light should appear on your Broadlink. It'll disappear once it's picked up an IR code.

Select Store to save the newly learnt code. (This is a step I wish to remove in future)

Select Activate to transmit the code

# Disclaimer
This is my solution to a problem many people seem to be struggling with. I've tried to make it as simple as possible and remove as much need for messing around with code as possible.

I'm new to developing apps and device handlers for the SmartThings hub and to the Groovy programming language.

As such there are a whole bunch of improvements that I would like to make now I've got this far such as:

* Not having to treat each code as a new device. This would be a nightmare for a TV remote.
* Being able to auto detect the MAC address of the device.
* Automatically storing the codes once detected
* Adding a Frequency Scan option for RF codes

If you have any other suggestions or care to contribute please let me know.

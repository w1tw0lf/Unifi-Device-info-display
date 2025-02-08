## INFO

This is a place to share ideas on how to create cards for the integration [Unifi-Device-info](https://github.com/w1tw0lf/Unifi-Device-info)

### Requirements

You will need the following 2 cards added via HACS

[lovelace-multiple-entity-row](https://github.com/benct/lovelace-multiple-entity-row)

[lovelace-card-mod](https://github.com/thomasloven/lovelace-card-mod)

### 1. Switch card

![image](https://github.com/user-attachments/assets/7e3f796e-a40a-48b6-8042-4d4f3ee4b97f)

Use [switch](https://github.com/w1tw0lf/Unifi-Device-info-display/blob/main/Switch%20card.yaml)

Replace 'switch name' with the name off your sensor for the switch

### 2. AP Card

![image](https://github.com/user-attachments/assets/ce689902-e7d4-4d9a-8c6d-27bb78a62a57)

Use [AP](https://github.com/w1tw0lf/Unifi-Device-info-display/blob/main/AP%20card.yaml)

Replace 'AP name' with the name off your sensor for the AP

### Picture Icon

To get an icon to display, add the png files in [PNG](https://github.com/w1tw0lf/Unifi-Device-info-display/tree/main/Entity%20Pictures) to config/www/unifi icons/. Then create config/customize.yaml.

In the file add the following:
```
sensor.*name*:
  entity_picture: /local/unifi icons/*.png
```
Replace *name* and *.png with as needed. Do so for each devices.

Add to configuration.yaml
```
homeassistant:
  customize: !include customize.yaml
```  
Reboot and the device should have a picture displayed as an icon.


## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to improve this integration.

## License

This project is licensed under the [MIT License](LICENSE).

## Disclaimer

This integration is provided "as is" without any warranty. Use it at your own risk.

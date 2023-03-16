[![hacs_badge](https://img.shields.io/badge/HACS-Custom-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)

# Home Assistant Sun card
Home Assistant Sun card based on Google Weather design

## Preview
![Light mode preview](https://user-images.githubusercontent.com/6829526/118412152-54d93900-b690-11eb-8b2b-e87b4cbcca7f.png)
![Dark mode preview](https://user-images.githubusercontent.com/6829526/118412162-64f11880-b690-11eb-9bd7-b8c6c7d8efd8.png)

## Requirements
- This card uses [Sun integration](https://www.home-assistant.io/integrations/sun/) so it needs to be enabled

## Install
### HACS (recommended)

Home Assistant Sun card is available as a custom repository on HACS.
In order to install it, please follow these steps:
1. Ooen HACS in your Home Assistant
1. Click on the 3-dots menu in the top right and select "Custom repositories"
1. Use the following information:
    - Repository: https://github.com/edwardtfn/home-assistant-sun-card
    - Category: Lovelace
1. Click "Add"
1. Search for "Sun card" on HACS directory and select the entry related to this card
1. Click "Download"
1. Follow the instructions from HACS and reload the page at the end

Note: I'm working on publishing this back into HACS default directory and will update the status here.

### Manually
1. Download the `home-assistant-sun-card.js` file from the [latest release available](https://github.com/edwardtfn/home-assistant-sun-card/releases) and save it in your `config/www/community/home-assistant-sun-card/` folder.
1. Go to `Settings > Dashboard` in Home Assistant
    1. Click on the 3-dots menu in the top right and select `Resources`.
    1. Click on the button `+ Add resource`.
    1. Add `/local/community/home-assistant-sun-card/home-assistant-sun-card.js` to the URL.
    1. Choose `Javascript Module` as Resource type.

## Set up
### Using UI
1. Go to your dashboard, enter in edit mode and click on `Add card`, you should be able to find `Custom: Sun card` in the list.
1. Once in the UI editor you can modify the card behavior by adding some of the config that you will find below

Note: If `Custom: Sun card` doesn't appear you will have to reload cleaning the cache.

### Using YAML
1. You just need to add a new card with `type: 'custom:sun-card'` to your cards list and any of the config that you will find below if you want to customize more your card.

Note: If you get an error similar to this `Custom element doesn't exist` you will have to reload cleaning the cache.

## Config
| Name          | Accepted values      | Description                          | Default                                             |
|---------------|----------------------|--------------------------------------|-----------------------------------------------------|
| darkMode      | `boolean`            | Changes card colors to dark or light | Home assistant dark mode state                      |
| language      | `string`<sup>1</sup> | Changes card language                | Home assistant language or english if not supported |
| showAzimuth   | `boolean`            | Displays azimuth in the footer       | `false`                                             |
| showElevation | `boolean`            | Displays elevation in the footer     | `false`                                             |
| timeFormat    | `'12h'`/`'24h'`      | Displayed time format                | Locale based on Home assistant language             |
| title         | `string`             | Card title                           | Doesn't display a title by default                  |         |

(<sup>1</sup>) Supported languages: `da`, `de`, `en`, `es`, `et`, `fi`, `fr`, `hu`, `it`, `nl`, `pl`, `pt-BR`, `ru`, `sl`, `sv`

## Known issues
- Home assistant seems to provide next events instead today's one 

## References
=> This repo was duplicated from [AitorDB/home-assistant-sun-card](https://github.com/AitorDB/home-assistant-sun-card) which was archived on 2023-03-10.

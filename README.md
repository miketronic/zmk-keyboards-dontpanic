# 10x2 ZMK Module

This repository contains the shield files for [10x2](https://github.com/miketronic/10x2) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

# Usage

Edit your west.yml file found in your zmk-config's config directory to add the 10x2 module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: caksoylar
      url-base: https://github.com/caksoylar
    - name: miketronic
      url-base: https://github.com/miketronic
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-rgbled-widget
      remote: caksoylar
      revision: main
    - name: zmk-keyboards-10x2
      remote: miketronic
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

# Notes



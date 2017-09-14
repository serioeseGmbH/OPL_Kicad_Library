# OPL_Kicad_Library

This is the Kicad Library for OPL components. Hope it can be a helper for you.  For any suggestion, please drop us a note at Ivy.li@seeed.cc

## Resources
1. A KiCad Bill-of-Materials (BOM) plugin to follow SeeedStudio's Fusion PCBA assembly service's template, This plugin is set up to use the KiCad schematic's part data as it is provided in Seeed Studio's Open Parts Library (OPL) collection for KiCad. - https://github.com/imrehg/kicad-bom-seeedstudio


[![Analytics](https://ga-beacon.appspot.com/UA-46589105-3/OPL_Kicad_Library)](https://github.com/igrigorik/ga-beacon)

## How To add SKU and MPN Field to Components Library

1. Install kifield
```bash
$ sudo pip2.7 install kifield
```
2. Extract fields from library into CSV file
  ```bash
  $ kifield -x my_cool_new.lib -i fiels.csv
  ```
3. Edit CSV file
    1. Add `,SKU,MPN` to end of the table head (first line)
    2. Add according values to end of each part in each line
4. Insert fields from CSV file into the library
```bash
$ kifield -i my_cool_new.lib -x fiels.csv
```
5. Delete CSV file (or use a difference CSV file name each time)
```bash
$ rm fiels.csv
```

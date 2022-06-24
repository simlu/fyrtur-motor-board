# Deploy

## Ubuntu

- Install stlink tools with `sudo apt install stlink-tools`
- Connect the five cables to the st link v2
- Plug in st link v2 into usb port
- run `st-info --probe`, you should see output that contains `descr: F0 small device`. This is important.
  If you don't see this output you might have waited too long and the blind went into sleep mode.
- Connect in power source for blind only after running above command
- To deploy run run `st-flash write build/fyrtur-motor-board.bin 0x8000000`
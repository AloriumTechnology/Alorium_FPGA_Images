# Alorium_FPGA_Images
Repository for officially released and beta/unreleased FPGA images that can be used with Alorium Technology's FPGA-based boards.

## Loading new FPGA Images

There are a few ways that new images can be loaded to the FPGA on Alorium's boards:

- Arduino IDE
- Command line
- RPD Image Webloader

### Arduino IDE
All of the officially released FPGA images for our boards are available through the
Tools dropdown menu in the Arduino IDE.  Updating the images is as easy as connecting
your board, selecting an image, and clicking "Burn Bootloader".  

Detailed instructions for doing this can be found in this YouTube tutorial:

[How to Update XLR8/Snō Board Package in Arduino IDE](https://youtu.be/OsKAWWdKsxM)

<a href="http://www.youtube.com/watch?feature=player_embedded&v=OsKAWWdKsxM
" target="_blank"><img src="http://img.youtube.com/vi/OsKAWWdKsxM/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="480" height="360" border="2" /></a>

### Command Line
The FPGA image is uploading using a utility we provide in our Arduino board package
called xlr8reconfig. This program can be run from outside of Arduino for any RPD 
image you wish to load.

The program is located in tools directory for the Alorium board package in the Arduino
installation path.  This differs a little bit based on operating system.  The following 
paths represent where the tool likely lives for default installtions:

```
macOS: [USER]/Library/Arduino15/packages/alorium/tools/xlr8reconfig/1.3.0/xlr8reconfig

Windows: [USER]\AppData\Local\Arduino15\packages\alorium\tools\xlr8reconfig\1.3.0\xlr8reconfig

Linux: [USER]/Library/Arduino15/packages/alorium/tools/xlr8reconfig/1.3.0/xlr8reconfig
```

The command line options for the xlr8reconfig tool are as follows:

```
usage: xlr8reconfig [-h] [-v [VERBOSE]] [-p PORT | --list_ports]
                    [--rpd_file RPD_FILE] [--load_image {0,1}]
                    [--baud_rate BAUD_RATE]

Connect to board through USB

optional arguments:

  -h, --help            Show this help message and exit

  -v [VERBOSE], --verbose [VERBOSE]
                        Increase verbosity. ex: -v, -vv, -vvv, -v 2

  -p PORT, --port PORT  Required: specify port from command line

  --list_ports          Optional: list out ports available and exit

  --rpd_file RPD_FILE   Required: specify rpd file name to use to program XLR8

  --load_image {0,1}    Forces xlr8 to load selected image. 
                        1 = load application image,         <--- USE THIS!!!
                        0 = load factory image              <--- don't use this

  --baud_rate BAUD_RATE
                        Optional: Define serial transmission baud rate.
                        Default = 115200
```

### RPD Image Webloader
If you are feeling adventurous, you can also try our Beta web-based RPD Image loader.

You can learn more about that process here:

[How to Update FPGAs Over the Web with the Alorium Web Loader](https://youtu.be/_GwRZJImrWo)

<a href="http://www.youtube.com/watch?feature=player_embedded&v=_GwRZJImrWo
" target="_blank"><img src="http://img.youtube.com/vi/_GwRZJImrWo/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="480" height="360" border="2" /></a>

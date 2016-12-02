Pynq / SDSoC installation

Follow the link on the voucher you bought with the pynq board, fill in the information. Receive the email, download the .lic file to your machine, then follow the link in that email for instructions to install it.

The only supported Ubuntu release seems to be 14.04.

I downloaded the file Xilinx_2016.2_sdsoc_0716_1_Lin64.bin (zipped), then did this:

 ```
 $ chmod +x ./Xilinx_2016.2_sdsoc_0716_1_Lin64.bin
 $ sudo bash 
 # source ./Xilinx_2016.2_sdsoc_0716_1_Lin64.bin
 ```

As documented in the release notes, you'll have to source the file /opt/Xilinx/SDSoC/2016.2/settings64.sh every time you log in to set paths. I added this line to my .bashrc:

 ```
 source /opt/Xilinx/SDSoC/2016.2/settings64.sh
 ```

The documents tell you to start it from the 'Start" menu or desktop, but there are no start icons installed. You can start it directly using this path:

/opt/Xilinx/SDSoC/2016.2/bin/sdsoc

In my case, it complained that I don't have a license and asks me to run the Vivado License Manager. Rerunning the license manager and copying the license again did not help.

You can run Vivado License Manager with the "vlm" command.

What did help is simply manually copying the .lic file to ~/.Xilinx/
Note the initial capital X in the directory name.



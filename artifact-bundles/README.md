# SLES12 and SLES15 artifacts for ImageStreamer v6.10 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v6.10 and below release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases
- Following version of SLES is supported
	- SLES 12 SP1 
	- SLES 12 SP2 
	- SLES 12 SP3 
	- SLES 12 SP4 
	- SLES 12 SP5
	- SLES 15 SP1 
	- SLES 15 SP2

## EFI based artifacts


With the EFI based artifacts, ImageStreamer can support all the filesystems including XFS/BTRFS for SLES Operating system.
This was not possible earlier because, Guestfish, used to customize the boot volume of the operating system, did not support XFS/BTRFS. 

Until now the root partition was mounted in the plan scripts, but now, to enable deployment using FAT32,  mount the partition (/boot/efi) and run the plan scripts through it for personalization, which provides support for all the filesystems.

## Version history
- HPE-SLES15-EFI-2020-10-28-v6.10.zip
	- Has fix for SSH not getting connected
	- Supports only systemd boot process
- HPE-SLES12-EFI-2020-04-02-v6.10.zip
	- HPE-SLES12-EFI-2020-04-02-v6.10.zip

# Prerequisite for using EFI Based Artifact bundle

## Note: 
- Please make sure to change Filesystem Attribute in the Server Profile creation page to desired filesystem type "only when you have a external drive attached to the blade"
- If you do not have a external hard drive attached to the blade please leave the default "disabled" option of filesystem attribute as is.
- LVM should be created at the time of installing the OS, on the bare metal, before image capture is done. The Filesystem type attribute in the Server Profile Page will not create LVM on the golden image which gets mounted, at the time of deployment.

## Golden Image creation for EFI based deployment of SLES12/SLES15:

1.	Ensure that you have access to SLES12/SLES15 ISO installation file containing iSCSI device drivers.

2.	Create a server profile with “HPE - Foundation 1.0 - create empty OS Volume” as OS Deployment plan and any available server 		hardware. Set an appropriate value for volume size in MiB units. The HPE Synergy Server will be configured for access to this 		empty OS Volume.

3.	Launch iLO Integrated Remote Console of this server and set SLES12/SLES15 ISO file as virtual CD-ROM/DVD image file. Power on 		the server.

4.	Hit "e" on the install disk before loading the kernel, edit the linuxefi ( if using EFI) or kernel (if using legacy), and add 		the kernel parameter “withiscsi=1 netsetup=1”. If the parameter is not entered, the iSCSI boot may fail.

5.	SLES installation starts and SLES installer detects the configured empty OS Volume as an iSCSI disk device. Select this iSCSI 		disk device as the target for SLES installation.

6.	Follow onscreen instructions and complete the SLES installation.

7.	After the OS boots up Create the following directories.

      -	mkdir -p /boot/efi/EFI/HPE/isdeploy
      -	mkdir –p /boot/efi/EFI/HPE/isdeploy/{scripts,tmp,data}
      
 
 8.	To make personalization work a systemd process needs to be created which will call the wrapper script. Please fallow below steps 	 for creating a systemd process 
  
       - cd /etc/systemd/system/
       - vi personalization.service (add Below line in this file save and exit)
	
		[Unit]
		Description=Personalization
		After=network-online.target

		[Service]
		Type=oneshot
		RemainAfterExit=yes
		WorkingDirectory=/boot/efi/EFI/HPE/isdeploy/
		ExecStart=/bin/bash HPE-ImageStreamer.bash

		[Install]
		WantedBy=multi-user.target

9.	Enable the service "systemctl enable personalization.service"

10.	Power off the server. 

11.	Navigate to HPE Synergy Image Streamer -> Golden Images and Click ‘Create Golden image’ 
 
12.	Select the OS volume corresponding to the server profile created for empty OS volume and choose “HPE - Foundation 1.0 - capture 	OS Volume as is” as the capture build plan. 
 
13.	HPE Synergy Image Streamer captures SLES image and adds it as a golden image.


## Follow the below document to load driver for HPE Virtual Connect SE 100Gb F32 Module for Synergy or HPE Synergy 50Gb Interconnect Link Module.

- https://github.hpe.com/ImageStreamer/image-streamer-sles/blob/v6.10/docs/HPE%20Synergy%20ImageStreamer%20Documentation%20to%20load%20drivers%20on%20SLES12%20during%20OS%20installation.pdf



## Artifact Bundle Contents

--------------------------------------------------------------------------------

                    File name: HPE-SLES12-EFI-2020-04-02-v6.10.zip
                Name (in manifest): HPE-SLES12-EFI-2020-04-02-v6.10
                       Description: ImageStreamer artifacts for SLES 12 using FAT32 partition (/boot/efi) personalization. (c) Copyright 2017-2020 Hewlett Packard Enterprise Development LP. Licensed under the Apache License, Version 2.0 (the \"License\");you may not use this file except in compliance with the License.You may obtain a copy of the License..
                             Dated: 2020-02-13 (02:42:42)

--------------------------------------------------------------------------------

Build Plans:

               Name: HPE-SLES12-EFI-BONDING-2020-04-02 (Type:deploy)
        Description: Configures SLES 12 by staging scripts in EFI partition. (c) Copyright 2019-2020 Hewlett Packard Enterprise Development LP Licensed under the Apache License, Version 2.0 (the "License")


               Name: HPE-SLES12-EFI-MultiNIC-2019-06-11 (Type:deploy)
        Description: Configures SLES 12 by staging scripts in EFI partition. (c) Copyright 2019-2020 Hewlett Packard Enterprise Development LP Licensed under the Apache License, Version 2.0 (the "License");...



Plan Scripts:

               Name: HPE-SLES12-EFI-unmount-2018-09-25 (general)
           FullName: 0cc203f4-371e-490c-aa7b-8babe4d38c4c_planscript.json
        Description: Unmounts EFI partition


               Name: HPE-SLES12-EFI-configure-hostname-2019-04-25 (deploy)
           FullName: 24c27dc0-b3fc-4a32-8d0e-5a1b7fd3a89f_planscript.json
        Description: Configures Hostname and Domain Name


               Name: HPE-SLES12-EFI-configure-users-2018-09-25 (deploy)
           FullName: 49f044df-76c3-4142-ac02-22ebbf1c1bbb_planscript.json
        Description: Creates users and set password


               Name: HPE-SLES12-EFI-LVM-2019-05-15 (deploy)
           FullName: 50e4fa71-8b9f-45b8-a3cc-d4bbb88d6336_planscript.json
        Description: LVM configuration using /boot/efi


               Name: HPE-SLES12-EFI-manage-ssh-service-2018-05-15 (deploy)
           FullName: 65fb4c1c-9504-4216-a0ce-abf79b0bbe99_planscript.json
        Description: Enables or Disables SSH


               Name: HPE-SLES12-EFI-mount-2018-09-25 (general)
           FullName: 82c17659-e96b-46ea-860d-a66a8a00d467_planscript.json
        Description: Mount EFI Partition


               Name: HPE-SLES12-EFI-configure-bonding-2019-04-25 (deploy)
           FullName: 8e92ebb4-5139-44de-b062-86f8fa5b10c4_planscript.json
        Description: This Scripts configures Mgmt and Deployment NIC Teaming


               Name: HPE-SLES12-EFI-configure-multiple-NICs-2019-06-05 (deploy)
           FullName: a7cc8b66-f447-4c0f-8960-85a20bdb1a02_planscript.json
        Description: Upload bash scripts to configure multiple NICs  to EFI partition directories /EFI/HPE/isdeploy/scripts and  /EFI/HPE/isdeploy/tmp


               Name: HPE-SLES12-EFI-wrapper-2019-03-24 (deploy)
           FullName: e4cadeaa-72af-4bb6-afdb-2b5d556fc6cf_planscript.json
        Description: Upload SUSE based wrapper script to execute OS volume personalization on first boot


               Name: HPE-SLES12-EFI-ibftBonding-2020-04-02 (deploy)
           FullName: fcae8a6d-2f55-4ad3-abd4-a9157a359eec_planscript.json
        Description: configures a  IBFT bonding service





--------------------------------------------------------------------------------

                    File name: HPE-SLES15-EFI-2020-10-28-v6.10.zip
                Name (in manifest): HPE-SLES15-EFI-2020-10-28-v6.10
                       Description: ImageStreamer artifacts for SLES 15 using FAT32 partition (/boot/efi) personalization. (c) Copyright 2017-2020 Hewlett Packard Enterprise Development LP. Licensed under the Apache License, Version 2.0 (the \"License\");you may not use this file except in compliance with the License.You may obtain a copy of the License..
                             Dated: 2020-09-09 (03:35:16)

--------------------------------------------------------------------------------

Build Plans:

               Name: HPE-SLES15-EFI-MultiNIC-2019-06-11 (Type:deploy)
        Description: Configures SLES 15 by staging scripts in EFI partition. This buildplan configures Multiple NIC's for Management connection (c) Copyright 2019-2020 Hewlett Packard Enterprise Development LP Licensed under the Apache License, Version 2.0 (the "License");...


               Name: HPE-SLES15-EFI-BONDING-2020-04-02 (Type:deploy)
        Description: Configures SLES 15 by staging scripts in EFI partition. This buildplan configures HA for iSCSI boot connections and Bonding of Management connections (c) Copyright 2019-2020 Hewlett Packard Enterprise Development LP Licensed under the Apache License, Version 2.0 (the "License")



Plan Scripts:

               Name: HPE-SLES15-EFI-configure-bonding-2019-04-25 (deploy)
           FullName: 120a972b-80f7-4667-8cc9-04085a2f2e83_planscript.json
        Description: This Scripts configures Mgmt and Deployment NIC Teaming


               Name: HPE-SLES15-EFI-unmount-2018-09-25 (general)
           FullName: 342336da-ba31-44b5-98f9-df4737e1a269_planscript.json
        Description: Unmounts EFI partition


               Name: HPE-SLES15-EFI-ibftBonding-2020-04-02 (deploy)
           FullName: 615a6c08-58e0-4efa-b893-f744f9d7a9ec_planscript.json
        Description: configures a  IBFT bonding service


               Name: HPE-SLES15-EFI-wrapper-2019-03-24 (deploy)
           FullName: 7055c154-9811-4512-b42f-ac5e05f41a5e_planscript.json
        Description: Upload SUSE based wrapper script to execute OS volume personalization on first boot


               Name: HPE-SLES15-EFI-manage-ssh-service-2020-08-24 (deploy)
           FullName: 7418dac4-e321-46b8-8d05-d9219aa1bd42_planscript.json
        Description: Enables or Disables SSH


               Name: HPE-SLES15-EFI-configure-multiple-NICs-2019-06-05 (deploy)
           FullName: 8478f6bc-69fc-4c91-bf4c-a132767b9068_planscript.json
        Description: Upload bash scripts to configure multiple NICs  to EFI partition directories /EFI/HPE/isdeploy/scripts and  /EFI/HPE/isdeploy/tmp


               Name: HPE-SLES15-EFI-configure-users-2018-09-25 (deploy)
           FullName: 85ccd05f-c70d-472c-8cf3-4f2adb2447a0_planscript.json
        Description: Creates users and set password


               Name: HPE-SLES15-EFI-mount-2018-09-25 (general)
           FullName: 90b89565-6ea3-4e56-acc7-a33fdd351571_planscript.json
        Description: Mount EFI Partition


               Name: HPE-SLES15-EFI-configure-hostname-2019-04-25 (deploy)
           FullName: bafd5605-6890-422c-886a-42846c53faad_planscript.json
        Description: Configures Hostname and Domain Name


               Name: HPE-SLES15-EFI-LVM-2019-05-15 (deploy)
           FullName: d03e2e7c-047b-4f57-a877-4c6308f73578_planscript.json
        Description: LVM configuration using /boot/efi


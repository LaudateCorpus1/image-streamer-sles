# SLES12/15 artifacts for ImageStreamer v5.2 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v5.2 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases
- The following SLES versions are supported
	- SLES 12 SP1
	- SLES 12 SP2
	- SLES 12 SP3
	- SLES 12 SP4
	- SLES 15 SP1
	- SLES 15 SP2
	
## Version history

HPE-SLES12-EFI-2020-04-02-v5.2.zip 
 - Artifact bundle for SLES12 for v5.2
 
HPE-SLES15-EFI-2020-04-02-v5.2.zip
 - Artifact bundle for SLES15 for v5.2

## EFI based artifacts

With the EFI based artifacts, ImageStreamer can support all the filesystems including XFS/BTRFS for SLES Operating system.
This was not possible earlier because, Guestfish, used to customize the boot volume of the operating system, did not support XFS/BTRFS. 

Until now the root partition was mounted, but now, to enable UEFI based deployment, the EFI partition, (/boot/efi) is mounted using the plan scripts for personalization, which provides support for all the filesystems.

# Prerequisite for using EFI Based Artifact bundle

## Note: 
- ***A new Golden Image needs to be created for using EFI based artifact bundle. Any existing Golden Images created using earlier releases of artifact bundle will not work with EFI artifact bundle. Follow the below steps to capture the Golden Image for SLES12/SLES15.***

( In case of HPE Vitual Connect SE 100Gb F32 Module or HPE Synergy 50Gb Interconnect Link Module hardware, follow the steps given in the linked document to load the driver and capture the golden image.https://github.com/HewlettPackard/image-streamer-sles/blob/v5.2/docs/HPE%20Synergy%20ImageStreamer%20Documentation%20to%20load%20drivers%20on%20SLES12%20during%20OS%20installation.pdf )

- If you do not have a external hard drive attached to the blade please leave the default "disabled" option of filesystem attribute as is. Please make sure you change Filesystem Attribute in the Server Profile creation page to desired filesystem type "only when you have a external drive attached to the blade".

- LVM should be created at the time of installing the OS, on the bare metal, before image capture is done. The Filesystem type attribute in the Server Profile Page will not create LVM on the golden image which gets mounted, at the time of deployment.

## Golden Image creation for EFI based deployment of SLES12/SLES15:

1.	Ensure that you have access to SLES12/SLES15 ISO installation file containing iSCSI device drivers.

2.	Create a server profile with “HPE - Foundation 1.0 - create empty OS Volume” as OS Deployment plan and any available server 		hardware. Set an appropriate value for volume size in MiB units. The HPE Synergy Server will be configured for access to this 		empty OS Volume.

3.	Launch iLO Integrated Remote Console of this server and set SLES ISO file as virtual CD-ROM/DVD image file. Power on the 		server.

4.	SLES installation starts and SLES installer detects the configured empty OS Volume as an iSCSI disk device. Select this iSCSI 		disk device as the target for SLES installation.

5.	Follow onscreen instructions and complete the SLES installation.

6.	After the OS boots up Create the following directories.

      - mkdir /boot/efi/EFI/HPE
      -	mkdir –p /boot/efi/EFI/HPE/isdeploy
      -	mkdir –p /boot/efi/EFI/HPE/isdeploy/scripts
      -	mkdir –p /boot/efi/EFI/HPE/isdeploy/tmp
      -	mkdir –p /boot/efi/EFI/HPE/isdeploy/data

7.	Modify /etc/init.d/after.local. Add below line

      -	sh /boot/efi/EFI/HPE/isdeploy/HPE-ImageStreamer.bash

8.	Change permission of the after.local file. (chmod 755 /etc/init.d/after.local)

9.	Power off the server. 

10.	Navigate to HPE Synergy Image Streamer -> Golden Images and Click ‘Create Golden image’ 
 
11.	Select the OS volume corresponding to the server profile created for empty OS volume and choose “HPE - Foundation 1.0 - capture 	OS Volume as is” as the capture build plan. 
 
12.	HPE Synergy Image Streamer captures SLES image and adds it as a golden image


## Artifact Bundle Contents

--------------------------------------------------------------------------------

	            File name: HPE-SLES12-EFI-2019-06-16-v5.0.zip
		Name (in manifest): HPE-SLES12-EFI-2019-06-16-v5.0
		       Description: ImageStreamer artifacts for SLES 12 using FAT32 partition (/boot/efi) personalization. 
		             Dated: 2019-07-08 (06:00:44)

--------------------------------------------------------------------------------

Build Plans:

	       Name: HPE-SLES12-EFI-MultiNIC-2019-06-11 (Type:deploy)
	Description: Configures SLES 12 by staging scripts in EFI partition. 


	       Name: HPE-SLES12-EFI-BONDING-2019-06-11 (Type:deploy)
	Description: Configures SLES 12 by staging scripts in EFI partition. 



Plan Scripts:

	       Name: HPE-SLES12-EFI-IbftBonding-2019-04-25 (deploy)
	   FullName: 0fc6fd1e-2f1b-429e-b5bb-86e960ac0b06_planscript.json
	Description: configure IBFT bonding


	       Name: HPE-SLES12-EFI-wrapper-2019-03-24 (deploy)
	   FullName: 135f7e5b-f56d-40cc-afbe-a45bb3c06e62_planscript.json
	Description: Upload SUSE based wrapper script to execute OS volume personalization on first boot


	       Name: HPE-SLES12-EFI-configure-bonding-2019-04-25 (deploy)
	   FullName: 22ebda69-95fe-49b7-94ce-4390b5445808_planscript.json
	Description: This Scripts configures Mgmt and Deployment NIC Teaming


	       Name: HPE-SLES12-EFI-LVM-2019-05-15 (deploy)
	   FullName: 2550912c-5dae-4970-953a-81f91f1ac3c0_planscript.json
	Description: LVM configuration using /boot/efi


	       Name: HPE-SLES12-EFI-configure-users-2018-09-25 (deploy)
	   FullName: 4485049e-95b9-4294-b647-2fe5075708e9_planscript.json
	Description: Creates users and set password


	       Name: HPE-SLES12-EFI-configure-multiple-NICs-2019-06-05 (deploy)
	   FullName: 6072a6f5-1fc3-473a-b350-f8185ec1e503_planscript.json
	Description: Upload bash scripts to configure multiple NICs  to EFI partition directories /EFI/HPE/isdeploy/scripts and  /EFI/HPE/isdeploy/tmp


	       Name: HPE-SLES12-EFI-configure-hostname-2019-04-25 (deploy)
	   FullName: 964ad19f-b576-4a1a-8a22-ae0aaeea97e4_planscript.json
	Description: Configures Hostname and Domain Name


	       Name: HPE-SLES12-EFI-mount-2018-09-25 (general)
	   FullName: b93f7798-34a7-4996-8db5-2fd258083a85_planscript.json
	Description: Mount EFI Partition


	       Name: HPE-SLES12-EFI-manage-ssh-service-2018-05-15 (deploy)
	   FullName: d73d05ae-9f16-4dda-8048-d0d5d1940a71_planscript.json
	Description: Enables or Disables SSH


	       Name: HPE-SLES12-EFI-unmount-2018-09-25 (general)
	   FullName: e73edb34-4161-45ae-9344-81dab4b545df_planscript.json
	Description: Unmounts EFI partition


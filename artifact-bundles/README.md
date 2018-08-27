# SLES12 artifacts for ImageStreamer v4.1 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v4.1 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history

HPE-SLES-12-2018-08-16-v4.1 - Fixed issue - ibftBond not getting created in SLES12 SP2

HPE-SLES-12-2018-05-10-v4.1.zip - Defect fixes

## Artifact Bundle Contents

--------------------------------------------------------------------------------
         File name: HPE-SLES-12-2018-08-16-v4.1.zip
         Name (in manifest): HPE-SLES-12-2018-08-16-v4.1
         Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
         Dated: 2018-06-28 (06:19:27)
--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-generalize-2018-05-10 (Type:capture)
	Description: Removes personalization settings from SLES 12.
	

	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2018-08-16 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings 


	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2018-05-10 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs. 



Plan Scripts:

	       Name: SLES-12-mount-and-validate - 2018-05-10 (general)
	   FullName: 1aa9cdfb-dbfc-4972-8c02-9db5b9c79467_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 29562bb3-687e-4709-a91c-71ae5b0676ff_planscript.json
	Description: configure NICs


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 388acd6b-5f6e-46c8-b2cd-ea3e6c4f75fb_planscript.json
	Description: remove network settings


	       Name: SLES-12-configure-users - 2018-01-22 (deploy)
	   FullName: 4549b981-1b63-4290-898a-26fedfcf69d7_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: 4b4ab67d-cc54-4729-aa00-d5f42f24c021_planscript.json
	Description: manage security services


	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: 537ecf76-9a4b-43c9-b06a-1cbb81759db6_planscript.json
	Description: remove user settings


	       Name: SLES-12-mount-generalize - 2018-05-10 (capture)
	   FullName: 68019d92-b03a-4cfc-917d-a174baa8e2e8_planscript.json
	Description: mount volume for generalization


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: 7c57b795-2d2e-4605-a55d-8cb7bafe2839_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: ac604fe0-020d-4d39-a134-2f328de13593_planscript.json
	Description: remove host configuration


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: c8a163a9-e443-43ae-8ace-9b85f7ef6cd2_planscript.json
	Description: configure LVM


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: d756e9bb-8c7c-4826-b068-8c96d308b8c9_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-configure-multiple-NIC-bonding-2018-08-16 (deploy)
	   FullName: ec8e85f6-412b-4611-994c-7b296ffd0c3b_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-configure-hostname-2017-12-21 (deploy)
	   FullName: ef4042dd-7684-4e0a-b27e-7722a48a91cd_planscript.json
	Description: configure hostname

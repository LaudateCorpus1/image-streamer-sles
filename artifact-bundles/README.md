# SLES12 artifacts for ImageStreamer v4.2 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v4.2 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history

HPE-SLES-12-2018-10-15-v4.2 - SLES artifact bundle for Image Streamer 4.2 

## Artifact Bundle Contents

--------------------------------------------------------------------------------

	            File name: HPE-SLES-12-2018-10-15-v4.2.zip
		Name (in manifest): HPE-SLES-12-2018-10-15-v4.2
		       Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
		             Dated: 2018-10-15 (10:25:33)

--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2018-10-15 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs. 


	       Name: SLES-12-generalize-2018-05-10 (Type:capture)
	Description: Removes personalization settings from SLES 12.


	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2018-08-13 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings 



Plan Scripts:

	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: 117d8e78-7f6e-4932-a740-b01696e90989_planscript.json
	Description: remove host configuration


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: 348e6414-f8db-48ae-912b-0e5a1004fc67_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: 352c23d9-0949-424b-b535-a1f9131a570b_planscript.json
	Description: configure LVM


	       Name: SLES-12-configure-multiple-NIC-bonding-2018-08-13 (deploy)
	   FullName: 3791df38-6429-47a4-9eed-c71df5c3b7af_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-mount-generalize - 2018-05-10 (capture)
	   FullName: 41f2461f-575c-4107-b61d-292b72da73d1_planscript.json
	Description: mount volume for generalization


	       Name: SLES-12-mount-and-validate - 2018-05-10 (general)
	   FullName: 5209e835-b803-478f-853c-286460c2e1c5_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 6356edfb-fd33-4cc3-a32f-c9d1ea04fe02_planscript.json
	Description: remove network settings


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: 7164ed05-d829-4f5f-9f7c-a829e33abe94_planscript.json
	Description: manage security services


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 8e39bf0c-42b8-48a0-891d-3c7be4e4b329_planscript.json
	Description: configure NICs


	       Name: SLES-12-configure-hostname-2017-12-21 (deploy)
	   FullName: 938a66d3-9f96-4736-bde6-ef9add278296_planscript.json
	Description: configure hostname


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: a2164a3c-e138-42fa-a321-66f9fbac5105_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-configure-users - 2018-01-22 (deploy)
	   FullName: c74c244a-0b79-4497-a8a8-9c93b747fc95_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: f04ae5f3-d4d4-4140-a16a-05cb7c04af9a_planscript.json
	Description: remove user settings





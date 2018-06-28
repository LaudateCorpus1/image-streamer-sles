# SLES12 artifacts for ImageStreamer v4.1 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v4.1 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history

HPE-SLES-12-2018-05-10-v4.1.zip 
- Defect fixes

## Artifact Bundle Contents

--------------------------------------------------------------------------------
         File name: HPE-SLES-12-2018-05-10-v4.1.zip
         Name (in manifest): HPE-SLES-12-2018-05-10-v3.1
         Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
         Dated: 2018-05-20 (13:34:00)
--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-generalize-2018-05-10 (Type:capture)
	Description: Removes personalization settings from SLES 12.
	           

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2018-05-10 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs. 


	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2018-05-10 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings 



Plan Scripts:
	       
	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: 07c7c4ba-1743-413a-9edb-f9d908d8ef5a_planscript.json
	Description: remove host configuration


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 0c15b12d-5b83-4c1a-ad1f-da3a81ac3791_planscript.json
	Description: remove network settings


	       Name: SLES-12-mount-and-validate - 2018-05-10 (general)
	   FullName: 0ffe6dfc-c932-4aa2-ae14-5de719e915fc_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 1f02b5ff-985b-429d-b35b-6519884c2fed_planscript.json
	Description: configure NICs


	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: 3d7da958-da33-4d3a-9fc2-06e24ba8dcd7_planscript.json
	Description: remove user settings


	       Name: SLES-12-configure-users - 2018-01-22 (deploy)
	   FullName: 6dac7c3b-25f6-4167-8ce2-b0356d99b166_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: 82e0b357-df4a-4f15-bf9e-3fe0faf77e40_planscript.json
	Description: configure LVM


	       Name: SLES-12-configure-multiple-NIC-bonding-2018-01-22 (deploy)
	   FullName: 948438b2-9f2d-4b02-a646-eec3941b44bc_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: b661b739-804c-4a9c-be8d-186afa93dfd1_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: b7e60065-b693-4488-9373-474423fc8a61_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-mount-generalize - 2018-05-10 (capture)
	   FullName: c439aeab-cc66-4d82-91b7-1f0387952783_planscript.json
	Description: mount volume for generalization


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: ef203053-9c38-460f-94da-1b508f1a4756_planscript.json
	Description: manage security services


	       Name: SLES-12-configure-hostname-2017-12-21 (deploy)
	   FullName: f27fb5b4-26dd-49fb-a084-87ab08cf1ab3_planscript.json
	Description: configure hostname

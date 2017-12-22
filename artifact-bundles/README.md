# SLES12 artifacts for ImageStreamer v4.0 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v4.0 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history

HPE-SLES-12-2017-12-21-v3.1.zip - Defect fixes

HPE-SLES-12-2017-08-22-v3.0.zip - Changed gateway ca to nic.gateway and fixed bond interface failover issues
 
HPE-SLES-12-2017-05-09.zip - Fixed character encoding issues

HPE-SLES-12-2017-03-24.zip - First version 

## Artifact Bundle Contents

--------------------------------------------------------------------------------

	            File name: HPE-SLES-12-2017-12-21-v3.1.zip
		Name (in manifest): HPE-SLES-12-2017-12-21-v3.1
		       Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
		             Dated: 2017-11-02 (12:17:44)

--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-generalize-2017-12-15 (Type:capture)
	Description: Removes personalization settings from SLES 12

	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2017-12-21 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings 

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2017-12-21 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs


Plan Scripts:

	       Name: SLES-12-mount-and-validate - 2017-03-15 (general)
	   FullName: 0f0ee367-f42b-4b5b-b0f5-b1f18e09fd5f_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 13a1cd05-2673-49bc-aac7-e24e5b124840_planscript.json
	Description: configure NICs


	       Name: SLES-12-mount-generalize - 2017-03-15 (capture)
	   FullName: 39b176a2-0137-4647-9072-83b24a59818b_planscript.json
	Description: mount volume for generalization


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: 449bff46-2589-4c24-a08d-5160ebd51dd6_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: 4dd1e5ea-462f-448f-aa63-5149ff93680f_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-configure-hostname-2017-12-21 (deploy)
	   FullName: 5a57067c-8905-4cf5-aea3-51689c7a4b91_planscript.json
	Description: configure hostname


	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: 5f545325-45c3-4515-bc4e-9ec0399b54a5_planscript.json
	Description: remove host configuration


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 65c4e3d8-93c6-4c33-b28c-167d473b9e01_planscript.json
	Description: remove network settings


	       Name: SLES-12-configure-users - 2017-03-15 (deploy)
	   FullName: 7a1877ba-9372-4761-8653-30ee316d0f74_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-configure-multiple-NIC-bonding-2017-12-06 (deploy)
	   FullName: 7aaa8d07-148f-4e15-aec9-45d221792785_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: 8cf35fd7-cda5-485f-8fa0-68776ca89c06_planscript.json
	Description: remove user settings


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: 9ac74b9b-2123-4f02-bedb-bdafb499b327_planscript.json
	Description: configure LVM


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: c3b6d09c-1d42-4ba1-ac83-47333f2f4007_planscript.json
	Description: manage security services






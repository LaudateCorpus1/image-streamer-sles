
# SLES12 artifacts for ImageStreamer v3.0 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v3.0 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history
HPE-SLES-12-2017-08-22-v3.0.zip - Changed gateway ca to nic.gateway and fixed bond interface failover issues
 
HPE-SLES-12-2017-05-09.zip - Fixed character encoding issues

HPE-SLES-12-2017-03-24.zip - First version 

## Artifact Bundle Contents

--------------------------------------------------------------------------------

	            File name: HPE-SLES-12-2017-08-22-v3.0.zip
		Name (in manifest): HPE-SLES-12-2017-08-22
		       Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
		             Dated: 2017-08-22 (07:20:01)

--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2017-08-22 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings

	       Name: SLES-12-generalize-2017-03-23 (Type:capture)
	Description: Removes personalization settings from SLES 12.

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2017-08-08 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs.

Plan Scripts:

	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: 09a095f4-057f-4faf-9606-91c49121d39a_planscript.json
	Description: remove user settings


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 125262d9-9e71-4a4f-bf5f-5a9d8d07c55d_planscript.json
	Description: configure NICs


	       Name: SLES-12-mount-and-validate - 2017-03-15 (general)
	   FullName: 3cdabe87-5ff7-41a8-984e-f2b05da07b26_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-configure-hostname-2017-08-08 (deploy)
	   FullName: 44cbe333-2143-4efc-9984-c58d848359cd_planscript.json
	Description: configure hostname


	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: 47f0cba3-10c7-40dd-aa30-403d3e6f3f33_planscript.json
	Description: remove host configuration


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: 727f4e4f-0d46-4470-b30e-1d30e170f750_planscript.json
	Description: configure LVM


	       Name: SLES-12-configure-multiple-NIC-bonding-2017-08-22 (deploy)
	   FullName: 8ea96dff-4f65-437e-a743-3202f3d07019_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-configure-users - 2017-03-15 (deploy)
	   FullName: 8fe901cc-b8f1-47ec-a6d5-22ed2182289c_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 93ffcaf7-84cf-4ead-964d-8a9bcc8ea9a7_planscript.json
	Description: remove network settings


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: be1f846a-220f-4f3b-9ad3-9670ac9d040a_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: d9b5d16b-57e7-452c-b073-07d73876f7c1_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: dfd97a50-2cfa-4ac2-a878-36ac5a19de2c_planscript.json
	Description: manage security services


	       Name: SLES-12-mount-generalize - 2017-03-15 (capture)
	   FullName: e56f2b89-1113-40e5-98fb-ba3857e485ff_planscript.json
	Description: mount volume for generalization


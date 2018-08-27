# SLES12 artifacts for ImageStreamer v4.0 release

## Note: 
- All artifact bundles in this repo are compatible with ImageStreamer v4.0 release
- Click on 'Branch:' drop down menu on this page to get artifact bundles for other ImageStreamer releases

## Version history
HPE-SLES-12-2018-08-23-v4.0.zip - Fixed ibftBond not getting created issue in SLES12 SP2

HPE-SLES-12-2017-12-21-v3.1.zip - Defect fixes

HPE-SLES-12-2017-08-22-v3.0.zip - Changed gateway ca to nic.gateway and fixed bond interface failover issues
 
HPE-SLES-12-2017-05-09.zip - Fixed character encoding issues

HPE-SLES-12-2017-03-24.zip - First version 

## Artifact Bundle Contents

--------------------------------------------------------------------------------
         File name: HPE-SLES-12-2018-08-23-v4.0.zip
         Name (in manifest): HPE-SLES-12-2018-08-23-v4.0
         Description: ImageStreamer artifacts for SLES 12 personalization and generalization. 
         Dated: 2018-07-05 (06:02:33)
--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2018-01-22 (Type:deploy)
	Description: Personalizes SLES 12 and configures NICs. 
	

	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP-2018-08-16 (Type:deploy)
	Description: Personalizes SLES 12 and configures NIC bondings


	       Name: SLES-12-generalize-2018-05-10 (Type:capture)
	Description: Removes personalization settings from SLES 12.
	            
	            
Plan Scripts:

	       Name: SLES-12-generalize-users - 2017-03-15 (capture)
	   FullName: 09b175b4-bd62-4b1b-bbdf-74f8667b40dc_planscript.json
	Description: remove user settings


	       Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
	   FullName: 1910def5-2c7e-4a78-b36c-11f36b996f18_planscript.json
	Description: configure LVM


	       Name: SLES-12-generalize-network - 2017-03-15 (capture)
	   FullName: 1a07b2f6-1890-4752-b3c7-511b8d16f36e_planscript.json
	Description: remove network settings


	       Name: SLES-12-configure-users - 2018-01-22 (deploy)
	   FullName: 26017177-6946-488e-b8e2-02b1a35d682c_planscript.json
	Description: set root password and create user accounts


	       Name: SLES-12-generalize-host - 2017-03-15 (capture)
	   FullName: 691a8a71-70fc-46cb-9700-623323b042a9_planscript.json
	Description: remove host configuration


	       Name: SLES-12-mount-and-validate - 2018-05-10 (general)
	   FullName: 87cce2c2-339d-4d0d-ae1d-e71bad1624f7_planscript.json
	Description: mount partition and validate the OS image


	       Name: SLES-12-configure-multiple-NICs - 2017-08-08 (deploy)
	   FullName: 9e0ccd10-48b0-4d35-940c-40d335f1f281_planscript.json
	Description: configure NICs


	       Name: SLES-12-configure-hostname-2017-12-21 (deploy)
	   FullName: a2828f97-ea2f-4c45-956c-6af29e56cd3c_planscript.json
	Description: configure hostname


	       Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
	   FullName: ba91e352-5798-4103-a5b6-7dde61577c1a_planscript.json
	Description: unmount volume after generalization


	       Name: SLES-12-unmount - 2017-03-15 (general)
	   FullName: bf84c4ef-2db4-4783-b207-d141b893eb8c_planscript.json
	Description: unmount partition after personalization


	       Name: SLES-12-configure-multiple-NIC-bonding-2018-08-16 (deploy)
	   FullName: c6445f84-fb48-4ef6-ae58-6a2d5551d979_planscript.json
	Description: configure NIC bondings


	       Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
	   FullName: d4f4c03e-8081-4620-ac72-7b351028e00e_planscript.json
	Description: manage security services


	       Name: SLES-12-mount-generalize - 2018-05-10 (capture)
	   FullName: dc5fbf4b-d46c-4313-a33d-9e7ce6bb8d72_planscript.json
	Description: mount volume for generalization

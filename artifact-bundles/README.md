# Artifact Bundle Contents

--------------------------------------------------------------------------------
         File name: HPE-SLES-12 - 2017-03-24.zip
         Name (in manifest): HPE-SLES-12 - 2017-03-24
       Description: ImageStreamer artifacts for SLES 12 personalization and generalization
             Dated: 2017-03-24 (16:39:45)
--------------------------------------------------------------------------------

Build Plans:

	       Name: SLES-12-generalize - 2017-03-23 (Type:capture)
	       Description: Removes personalization settings from SLES 12.

	       Name: SLES-12-personalize-and-configure-NICs-LVM-BP-2017-03-23 (Type:deploy)
	       Description: Personalizes SLES 12 and configures NICs.

	       Name: SLES-12-personalize-and-NIC-bondings-LVM-BP - 2017-03-23 (Type:deploy)
	       Description: Personalizes SLES 12 and configures NIC bondings



Plan Scripts:

               Name: SLES-12-generalize-users - 2017-03-15 (capture)
           FullName: 13f210d1-7c6c-4e6b-a0bb-a46bb24db1d5_planscript.json
        Description: remove user settings


               Name: SLES-12-configure-hostname-2017-03-15 (deploy)
           FullName: 197e304e-6441-4ba4-b5f1-8bc686947b41_planscript.json
        Description: configure hostname


               Name: SLES-12-generalize-network - 2017-03-15 (capture)
           FullName: 2393ec04-c23a-45cd-a749-b716b1ccc484_planscript.json
        Description: remove network settings


               Name: SLES-12-unmount - 2017-03-15 (general)
           FullName: 2891f4e9-8e73-42e2-a809-f4b9b8e3f12e_planscript.json
        Description: unmount partition after personalization


               Name: SLES-12-configure-multiple-NIC-bonding-2017-03-15 (deploy)
           FullName: 290ca503-908f-486e-b314-15e3add16922_planscript.json
        Description: configure NIC bondings


               Name: SLES-12-generalize-host - 2017-03-15 (capture)
           FullName: 477cb9fe-5fce-476b-9169-da7426116c3c_planscript.json
        Description: remove host configuration


               Name: SLES-12-mount-and-validate - 2017-03-15 (general)
           FullName: 4b628f53-7055-442a-8cf3-ddc8f4b4b8bd_planscript.json
        Description: mount partition and validate the OS image


               Name: SLES-12-configure-users - 2017-03-15 (deploy)
           FullName: 8ee3b32d-5460-495f-9e57-f5a65c07fd8f_planscript.json
        Description: set root password and create user accounts


               Name: SLES-12-manage-security-services - 2017-03-15 (deploy)
           FullName: a16b908f-7ca8-401c-9e35-a97210e9deeb_planscript.json
        Description: manage security services


               Name: SLES-12-mount-generalize - 2017-03-15 (capture)
           FullName: be9853b0-efdf-46e3-b966-321fbf4b9b92_planscript.json
        Description: mount volume for generalization


               Name: SLES-12-unmount-genralize - 2017-03-15 (capture)
           FullName: cddcbfb1-9130-4059-853d-968c32e70c4f_planscript.json
        Description: unmount volume after generalization


               Name: SLES-12-configure-multiple-NICs - 2017-03-15 (deploy)
           FullName: eb44d30f-4b3d-4f13-b3b5-aa1c37f7bc4a_planscript.json
        Description: configure NICs


               Name: SLES-12-configure-partition-using-LVM - 2017-03-15 (deploy)
           FullName: ebf1de98-de8f-4503-a648-155a00a9a3a8_planscript.json
        Description: configure LVM
        

# How to Export iCloud Photos and Fix Metadata

This guide will walk you through the process of exporting your iCloud photos to an external hard drive and fixing the metadata using a custom script.

## Prerequisites

- MacOS computer
- External hard drive
- Internet connection
- `update_xmp` script (provided separately)

## Steps

1. Open Photos.app on your MacOS.

2. Create a new Media Library on your external hard drive.

3. In Photos.app settings, change the storage option:
   - Go to Settings
   - Select "Store on Mac" instead of "Optimize Storage"

4. Wait overnight for all photos to download from iCloud.

5. Export photos with original metadata:
   - Select all photos (Cmd + A)
   - Choose "Export Original"
   - Select the following options:
     - Include XMP files
     - Export as Moments folders
   - Choose a location on your external hard drive
   - Wait approximately 20 minutes for the export to complete

6. Fix metadata using the `update_xmp` script:
   - Navigate to the main folder containing all exported Moments folders
   - Place the `update_xmp` file in this folder
   - Make the script executable:
     ```
     chmod +x update_xmp
     ```
   - Run the script:
     ```
     ./update_xmp
     ```

## Note

Ensure you have enough free space on your external hard drive for both the new Media Library and the exported photos.

## Troubleshooting

If you encounter any issues during the process, please check the following:
- Ensure your Mac is connected to power and has a stable internet connection
- Verify that you have sufficient storage space on your external hard drive
- Make sure you have the necessary permissions to execute the `update_xmp` script


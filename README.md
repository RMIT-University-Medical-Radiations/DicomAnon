# DicomAnon
This is a repository for a DICOM anonymiser, deftly named DicomAnon. Although there are many applications that will anonymise DICOM files, this one was written to do so in bulk. With DicomAnon, you can point to a parent folder containing many patient folders, which may contain many imaging sessions, which may contain images acquired with different modalities. After telling DicomAnon where you want the anonymised files to be placed, it will preserve the folder structure and place anonymised DICOM files there. DicomAnon does not change the original files; it merely reads them, changes the DICOM tags that contain personal information about the patient, and writes them to the designated destination folder.

Note that adding new patient folders (and updates to existing patient folders) will not erase previous DICOM files for the same patient; the new anonymised DICOM files will be saved in the same structure alongside those previously processed. The new patient IDs will also be added to the Excel mapping spreadsheet.

The DICOM files are anonymised by replacing the values of the following DICOM tags:
* PatientName
* PatientID
* PatientAddress
* PatientMotherBirthName
* EthnicGroup
* PatientIdentityRemoved
* ReferringPhysicianName
* ReferringPhysicianAddress
* StudyDescription
* SeriesDescription
* InstitutionName
* InstitutionAddress

On completion, DicomAnon will save as an Excel spreadsheet in your home folder a mapping of the true patient IDs to anonymised patient IDs.

## Installation
Unzip the downloaded file and move it to a convenient place, alongside your other utility applications.

## Usage
1. Select the parent folder of the patient folders containing the DICOM files to be anonymised.
2. Select the destination folder that will contain the anonymised DICOM files. Create a new destination folder if you wish.
3. Press the Anonymise! button.
4. Wait for the processing to complete. The progress bar provides a visual clue about how far along it is.
5. An Excel spreadsheet with the mapping from the real patient ID to the anonymised patient ID will be saved in your home directory.

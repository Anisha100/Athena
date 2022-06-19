# [FIDO2 Smart Card for Medical record maintenance and Temporary Token Authentication for in-house hospital patients](https://medical-record.centralindia.cloudapp.azure.com)

The importance of a good record cannot be undermined. A good medical record serves the interest of the medical practitioner as well as his patients.  Changing technology and legislation have ushered in a shift in healthcare which led to the discovery of several drawbacks and potential challenges. As the popularity of electronic health record storage grows, a special concern arises for the privacy and security of patient data. Hence we introduce AthenaMR, a seamless and fast web-based framework for leveraging digital data storage processes to sustainably serve patients from all backgrounds. It uses FIDO2 Smart Card for Medical record maintenance and Temporary Token Authentication for in-house hospital patients. It simplifies the entire storage process and can be accessed using NFC, BLE, or USB. Moreover, the private information never leaves the trusted device and prevents any sort of remote hijack. Under the theme of healthcare, this project is a web-based framework where we decided to come up with a FIDO2-based card that can change the world by making single-stop medical record storage instruments extremely seamless and secure compared to any other existing methods. 
![image](https://user-images.githubusercontent.com/87559560/174489972-2f5102c9-4848-4afe-a9f6-6fe4fd564dd7.png)

In this projectwe implement FIDO2, a recently evolved technology by FIDO Alliance which is on its way to prove itself to be
instrumental in Passwordless authentication frameworks. However, it can used for much more than
just authentication. This project proposes a centralized system for medical record maintenance of women in an extremely seamless, secure and easy to use manner.
 We aim to have a partnership with various hospitals. It guarantees easy record maintenance
and hence the patients will not have to go about the hospitals with an entire medical file.

## Contributors

1. [Anisha Ghosh](http://github.com/anisha100)
2. [Rishita Shaw](http://github.com/theseregrets)


## Objective

Users willing to use this service can buy a FIDO2 supported physical security key with USB and NFC
capabilities. Then register on our website to generate a unique username and register the FIDO2 key
along with it. The user portal contains the option to view and upload the medical reports. It is to be
noted that there is no way to delete already added reports. This is to prevent misguidance. There is
also an option to register a temporary token for authentication. This temporary token would be just an
NFC card which can be kept in the hospital files. The user must set an expiry date for the NFC card
after which it will be automatically disabled. A hospital while admitting a patient can request the
patient to register the smart card which can be kept in the hospital files so that the doctors can access
the patient records and add new reports after medical tests.
**The user has the option to disable the registered temporary tokens on discharge from the hospital to
prevent data misuse, and if not disabled manually, it will be automatically disabled when the
stipulated time has passed.**

## Features

The website will have two versions:

1. User version: This has the option to view records, add records, register and remove temporary
   tokens and register new FIDO2 keys.
2. Hospital version: This has only the options to view and add records. The hospital will not be
   authorized to manage tokens and keys. It is to be noted that the hospital can login only with
   temporary tokens.
3. For medical equipments: We provide an API endpoint with which medical devices and softwares 
   will be able to directly upload the report against an user. It is to be noted that the medical 
   equipments should preferably be interfaced with a NFC reader as the API endpoint authenticates 
   the device with it only. API Documentation [here](./apidoc.md)

## Tech Stacks
```bash
Technologies to be used:
• FIDO2 Specifications
• Web NFC
• Microsoft Azure.
```
## FAQ

FAQ:

1. What if the user loses the FIDO2 key? – She can login via Email OTP to assign new FIDO2
   key.
2. When the user is sick how can she login? – Since FIDO2 is a Passwordless technology, the
   family members of the user can use the security key.
3. What are the system requirements for the user? – Any android phone with Google Chrome
   89+ and NFC reader.
4. What are the system requirements for the hospital? – Android device with Google Chrome
   89+ and NFC reader. However, it is inconvenient for the hospital to use phone so any
   computer with NFC reader is supposed to work. Some laptops have NFC readers inbuilt, as
   well as USB NFC readers are available.
5. How will the reports be stored? – The reports will be stored as uploaded by the hospital in any
   file. We are intentionally not enforcing any file format as some medical records need to be
   stored as PDF, while some like the medical scans are stored as DICOM or other formats.

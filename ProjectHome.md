If a smartphone has a secure element (that may be used for NFC) - it should be possible to leverage this payment information to be able, to facilitate internet based payments.

A user is directed to the payment screen where an optical code such as a QR code or Data Matrix is displayed. The user then opens up the relevant payment application on their device, and scans the optical code. The code contains information such as the url to go access, to access payment (and maybe an symmetric SSL key). The application then access the URL, which will begin to perform a payment transaction with the Secure Element on the device (or credentials stored in another way, such as directly on the flash of the smart phone - this is however less secure and should not be advised). The user could be presented with a confirmation and then the transaction would complete and confirmation screen could be displayed.

The desktop or other computer browser would be using a system such as AJAX and then receive or poll a message that stated the payment had completed and then redirect to a confirmation screen.


The prototype for this project will be created with an Android application and Secure Element (if a phone is available that is able to be accessed), a web application could be created on Google Web Apps, with a simple transaction example. The Google application will communicate web the web app using a simple URL get for now and can be extended to a full TCP or web socket based approach later on.

This is intended as a system for users without an NFC reader on their desktop computer, but may be using an NFC based system with secure element on their smartphone device.
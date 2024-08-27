# html5-canvas-signature-submit
A basic sample of how to draw signature on HTML5 canvas and submit it to PHP script, save the image on a server folder and attach it on email.

## General description:

1. Capture the Canvas Drawing and Convert it to an Image
Use JavaScript to capture the signature drawn on the HTML5 canvas and convert it into a data URL (base64 encoded string). This data URL can then be sent via AJAX to your PHP script.

2. Send the Image to the Server via AJAX
You'll need to send the captured image data to the server using AJAX. The image will be sent as a string (base64 encoded) to the server-side PHP script.

3. Process the Image on the Server and Save it
On the server side, the PHP script will decode the base64 string back into an image and save it on the server.

4. Send the Image via Email
After saving the image, you can attach it to an email and send it.


## Code Explanation:

1. Canvas Drawing: The user draws their signature on the canvas. When they press the submit button, the canvas content is converted to a base64 encoded PNG image.

2. AJAX Submission: The base64 image data is submitted to the PHP script via AJAX.

3. PHP Processing:
	-The base64 string is decoded into raw image data.
	-The image is saved to the server.
	-The saved image is attached to an email and sent to a specified recipient.

4. Email Sending: The email is composed with the image as an attachment using multipart/mixed content type.

This code is a basic implementation and can be further customized according to your needs, such as adding error handling, improving the drawing experience, or securing the form.
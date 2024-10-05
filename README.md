
# QR Code Generator

The QR Code Generator project you are working on uses Java, Maven, and QRGen (a wrapper for the ZXing library) to create a QR code generator application. This project allows users to convert input text or URLs into QR codes, which can then be scanned by QR code readers. The generated QR codes are saved as PNG files, making them easy to share and use across different platforms.
## Prerequisites

- Java 8 or later.
- Apache Maven.
- QRGen library (wrapping ZXing).
## Features

- Text or URL Input: Converts plain text or URLs into scannable QR codes.
- Image Generation: Saves the generated QR codes as PNG image files.
- Scalability: It can generate QR codes of varying sizes depending on the input data.



## Applications

- Business Cards: Embedding contact details in QR codes.
- URLs and Links: Simplifying the process of sharing websites, links, or app download pages.
- Event Tickets: QR codes for ticket scanning at events.
- Authentication: Used in two-factor authentication systems to verify user identities.
## API Reference

The QR code generator project utilizes the following classes and methods from the QRGen library:

- QRCode
QRCode.from(String text)
Generates a QR code from the provided text or URL.

- QRCode.withSize(int width, int height)
Sets the size of the QR code. The width and height define the dimensions of the generated QR code image.

- QRCode.to(ImageType type)
Specifies the output format for the QR code image. Supported types include PNG, JPG, and GIF.

- QRCode.withColor(int foregroundColor, int backgroundColor)
Customizes the color of the QR code by specifying the foreground and background colors in ARGB format.

- QRCode.stream()
Streams the QR code data as a ByteArrayOutputStream, allowing it to be written to a file or directly used in memory.

- File Handling
File.createNewFile()
Creates a new empty file in the specified directory. This is used to save the generated QR code as an image.

- file.createNewFile();
FileOutputStream
A class that provides methods for writing data to a file. It is used to write the QR code's byte stream into a .png file.

- ByteArrayOutputStream.writeTo(OutputStream out)
Writes the byte data from the ByteArrayOutputStream to another OutputStream, such as a file stream.
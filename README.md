# Metadata Analysis – PwnTillDawn

## Objective
The objective of this task is to analyze hidden metadata and embedded information within different file types using various forensic tools.

---

# 1. ExifTool Analysis (Ocean.jpg)

ExifTool was used to extract metadata from the image file.

Command used:
exiftool Ocean.jpg

The output revealed metadata such as file information, creation date, and possible device details.

## Screenshot
![7c4c5f55-f8bc-4cb2-bb08-b0bdce5eb640](https://github.com/user-attachments/assets/f7b0646f-2579-4580-860f-bb2356cabd02)
![7430e8c3-c67c-41fc-b4c8-1632b5a876c9](https://github.com/user-attachments/assets/481e4e57-13b8-46b8-a06a-7d514752c278)

---

# 2. HexEditor Analysis (Computer.jpg)

HexEditor was used to inspect the raw data of the image file.

Command used:
hexedit Computer.jpg

This allows viewing of the file in hexadecimal format, which may reveal hidden or embedded data within the file.

## Screenshot
![1123df57-cfde-4a78-9b15-caa19822ef7b](https://github.com/user-attachments/assets/159cf20a-0b9c-46f7-adbf-3dc234f44581)

---

# 3. Binwalk Analysis (dog.jpg)

Binwalk was used to analyze and extract hidden or embedded files within the image.

Commands used:
binwalk dog.jpg  
binwalk -e dog.jpg  

The scan identified embedded data within the image. The extraction process revealed hidden files stored inside the original image.

## Screenshot
![d07847a6-f9e7-416d-8560-b90c75993e28](https://github.com/user-attachments/assets/0f3d9bd3-0e83-43e3-afe7-5629df6da77f)

---

# 4. Strings Analysis (computer.jpg)

The strings command was used to extract readable text from the image file.

Command used:
strings computer.jpg

This revealed human-readable strings that may contain hidden messages, URLs, or sensitive information.

## Screenshot
![7300eb77-819b-4e25-8eef-a976009d3453](https://github.com/user-attachments/assets/9ba1eba1-d02e-4f42-b50e-2e709d13056e)
![190322aa-9076-4732-b184-d2ec21508356](https://github.com/user-attachments/assets/4218b212-4d6b-4afb-8276-ef9add24ec12)

---

# 5. File Analysis (solitaire.exe)

The file command was used to determine the actual type of the file.

Command used:
file solitaire.exe

Result:
solitaire.exe: PNG image data, 640 x 449, 8-bit/color RGBA, non-interlaced

Analysis:

Although the file has a ".exe" extension, it is actually a PNG image file. This indicates that the file has been disguised by changing its extension.

This demonstrates that file extensions cannot be trusted and proper file analysis is required to determine the true file type.

## Screenshot
![b0a08858-a6aa-4c87-81ed-fb4f2becd40a](https://github.com/user-attachments/assets/ff949d54-5ea6-41d4-8630-238b7393972d)

---

# 6. File Analysis (rubiks.jpg)

The file command was used to verify the actual file type.

Command used:
file rubiks.jpg

The result confirms whether the file is a valid image or contains suspicious data.

## Screenshot
![a8410891-7f30-4867-813e-98f34792aa33](https://github.com/user-attachments/assets/f27927cc-c34b-4a81-b75b-34d4ca2792d6)

---

# Conclusion

Metadata analysis helps identify hidden information within files such as authorship, embedded data, and hidden messages.

Techniques such as ExifTool, HexEditor, Binwalk, Strings, and File analysis can reveal sensitive information that may not be visible normally.

This demonstrates the importance of analyzing files properly, as attackers may hide malicious or sensitive data inside seemingly harmless files.

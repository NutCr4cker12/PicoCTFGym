# Information
## Description
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](./cat.jpg)
### hints
1. Look at the details of the file
2. Make sure to submit the flag as picoCTF{XXXXX}
# Solution  
Started by checking the fileformat of the [cat.jpg](./cat.jpg) so it's actually a jpg file and not a txt file with wrong file extension naming:
```
$ file cat.jpg  
cat.jpg: JPEG image data, JFIF standard 1.02, ...
```
Okay, so it's an actual image. Quick look at the image itself so there's no "details" visible and no, just a cat. 

Googled how to extract/inspect meta data from jpg images and went with ```Exiftool```. The metadata didn't provide anything at the first clance and I had come back multiple times before I realized one of the metadata was actually base64 encoded. Missed it at first due to lack of trailing equality signs but now that it was discovered, decoding it via [CyberChef](https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)) resulted into the flag.
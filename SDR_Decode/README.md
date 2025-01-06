# SDR Decode 

## what needed 

### subject ([LUM-LT-RF-RGBW-01](https://shop.gsmet.be/Article/ArticleDetails/a050e3fa-6031-46fb-9c97-5524d6bc4817))
The target device is a **LED controller** that operates with an RF remote. The goal is to capture the communication between the remote and the controller and decode it as much as possible.  
The datasheet specifies that it uses the **433.92 MHz** frequency band.
### SDR ([RTL SDR](https://www.hfelectronics.be/shop/scanners/600-rtl-sdr.html))
A **low-cost USB stick SDR** is being used, which costs around €25 and supports the required frequency range.  
If the target operates on a higher or lower frequency, ensure the SDR can handle that range.

### SDR software ([SDR#](https://airspy.com/download/))
For software, I opted for **SDR# (SDRSharp)**

## Decoding 

### capturing

### analog to digital decode 
#### button one 

![](.\MISC\BTN_1_Decode.png)

```
100011101000100011101110111011101000100010001000111011101000111011101000100010001000100010001000100010001000
```

It looks like there are two symbols: `1000` and `1110`. When converting `1000` into `A` and `1110` into `B`, it transforms into this:

```
ABAABBBBAAAABBABBAAAAAAAAAA
```
Splitting it further into bytes gives:
```
ABAABBBB AAAABBAB BAAAAAAA AAA
```
If you replace it with `00` = A, `01` = B, `10` = C, and `11` = D, you get:
``` 
CADCCACADCDCDCDCCACACACADCDCCADCDCCACACACACACACACACACA
```
Splitting it further into bytes results in:
``` 
CADCCACA DCDCDCDC CACACACA DCDCCADC DCCACACA CACACACA CACACA
```
This seems to be more promising. However, there may have been a few `00` pairs discarded due to lack of context. It's also unclear where zeros were missed at the front or back of the sequence.

### digital to data decode

## Result 




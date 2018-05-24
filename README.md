# QR Code Decoder by Golang

This Project is Developing.

# Plan

1. Dynamic binarization
2. Increase the speed of picture scanning: OK
3. Fix the score: OK
4. Fault tolerant code correction data: OK
5. Data encoding method
    Numbert
    alphanumeric
    8-bit byte: OK
    Kanji
6. Identify two-dimensional codes that are tilted at each angle

# Example

```golang
fi, err := os.Open("qrcode.png")
if err != nil{
    logger.Println(err.Error())
    return
}
defer fi.Close()
qrmatrix, err := qrcode.Decode(fi)
if err != nil{
    logger.Println(err.Error())
    return
}
logger.Println(qrmatrix.Content)
```

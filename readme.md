# Winforms QR Example


![example](./resources/example.PNG)

## Get Started

`PM> Install-Package QRCoder`

```C#
public Form1()
    {
        InitializeComponent();

        QRCodeGenerator qrGenerator = new QRCodeGenerator();
        QRCodeData qrCodeData = qrGenerator.CreateQrCode("testnutzer;pass12_X4", QRCodeGenerator.ECCLevel.Q);
        QRCode qrCode = new QRCode(qrCodeData);
        Bitmap qrCodeImage = qrCode.GetGraphic(20);

        pictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;
        pictureBox1.Image = qrCodeImage;
    }
```



## Source

https://github.com/codebude/QRCoder
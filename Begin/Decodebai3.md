```Python
from PIL import Image

def extract_message(image_path):
    img = Image.open(image_path)
    binary_message = ''
    pixel_values = list(img.getdata())
    for pixel in pixel_values:
        for color_channel in range(3):
            binary_message += str(pixel[color_channel] % 2)
    message = ''.join(chr(int(binary_message[i:i+8], 2)) for i in range(0, len(binary_message), 8))
    return message
extracted_message = extract_message('C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\hidden_message.png')
print('Extracted Message:', extracted_message)
```

```Python
from PIL import Image
def hide_message(image_path, message):
    img = Image.open(image_path)
    binary_message = ''.join(format(ord(char), '08b') for char in message)
    data_index = 0
    for i in range(img.width):
        for j in range(img.height):
            pixel = list(img.getpixel((i, j)))
            for color_channel in range(3):
                if data_index < len(binary_message) and pixel[color_channel] % 2 != int(binary_message[data_index]):
                    pixel[color_channel] += 1
                data_index += 1
            img.putpixel((i, j), tuple(pixel))
    img.save('C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\hidden_message.png')
hide_message('C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\AES.jpg', 'CayCon')
```

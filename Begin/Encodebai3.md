```Python
from PIL import Image

def hide_message(image_path, message):
    img = Image.open(image_path)
    binary_message = ''.join(format(ord(char), '08b') for char in message)
    width, height = img.size
    data_index = 0
    for y in range(height):
        for x in range(width):
            pixel = list(img.getpixel((x, y)))
            for i in range(3):
                if data_index < len(binary_message):
                    pixel[i] &= ~1
                    pixel[i] |= int(binary_message[data_index])
                    data_index += 1
            img.putpixel((x, y), tuple(pixel))
    img.save('hidden_message_image.png')
    print('Đã giấu tin vào ảnh.')
image_path = 'C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\AES.jpg'
message_to_hide = 'CayCon'
hide_message(image_path, message_to_hide)
```

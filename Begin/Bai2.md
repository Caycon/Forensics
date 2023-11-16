```Python
from PIL import Image
img = Image.open(r"C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\AES.jpg")
pixel = img.load()

with open ("C:\\Users\\nbcta\\OneDrive\\Desktop\\Test\\Python\\New folder\\outputbai2.txt", "w") as f:
    for x in range(img.size[0]):
        for y in range(img.size[1]):
            r, g, b= pixel[x, y]
            f.write("[" + str(r) + "," + str(g) + "," + str(b) + "] ")
        f.write("\n")
```

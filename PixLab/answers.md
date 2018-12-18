A1
1. 8
2. 3 bytes
3. 307, 200

A2
1. R 255, G 105, B 255
2. R 255, G 253, B 99
3. R 255, G 36, B 255
4. R 255, G 255, B 255
5. R 50, G 50, B 50

A3
1. 0
2. 0
3. 639
4. 479
5. top to bottom
6. left to right
7. Yes

A5
1. No
2. Yes
3. No
4. Yes
5. Yes
6. Yes
7. No

A6

1.

public void mirrorVerticalRightToLeft() {
    Pixel[][] pixels = this.getPixels2D();
    Pixel leftPixel = null;
    Pixel rightPixel = null;
    int width = pixels[0].length;
    for (int row = 0; row < pixels.length; row++)
        for (int col = 0; col < width / 2; col++)
            leftPixel = pixels[row][col];
            rightPixel = pixels[row][width - 1 - col];
            leftPixel.setColor(rightPixel.getColor());
}

public static void testMirrorVerticalRightToLeft() {
    Picture caterpillar = new Picture("caterpillar.jpg");
    caterpillar.explore();
    caterpillar.mirrorVerticalRightToLeft();
    caterpillar.explore();
}


2. 


public void mirrorHorizontal() {
    Pixel[][] pixels = this.getPixels2D();
    Pixel topPixel = null;
    Pixel bottomPixel = null;
    int height = pixels.length;
    for (int col = 0; col < pixels[0].length; col++) {
        topPixel = pixels[row][col];
        bottomPixel = pixels[height - 1 - row][col]
        bottomPixel.setColor(topPixel.getColor());
    }
}


3.


public void mirrorHorizontalBotToTop() {
    Pixel[][]pixels = this.getPixels2D();
    Pixel topPixel = null;
    Pixel bottomPixel = null;
    int height = pixels.length;
    for (int col = 0; col < pixels[0].length; col++) {
        topPixel = pixels[row][col];
        bottomPixel = pixels[height - 1 - row][col];
        topPixel.setColor(bottomPixel.getColor());
    }
}


public static void testMirrorHorizontalBotToTop()
{
Picture caterpillar = new Picture("caterpillar.jpg");
caterpillar.explore();
caterpillar.mirrorHorizontalBotToTop();
caterpillar.explore();
}


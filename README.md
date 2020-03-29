[![Android Arsenal](https://img.shields.io/badge/Android%20Arsenal-StickerView-brightgreen.svg?style=flat)]() 
StickerView
=========

A view which can add sticker and zoom,drag,flip,delete it

## Screenshots
![](https://github.com/wuapnjie/StickerView/blob/master/screenshots/screenshot1.png)
![](https://github.com/wuapnjie/StickerView/blob/master/screenshots/screenshot2.png)

## Usage


**Tips**:StickerView extends FrameLayout
#### In layout
```xml
<com.xiaopo.flying.sticker.StickerView
        android:id="@+id/sticker_view"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_gravity="center">
    <!-- custom, maybe you will like to put an ImageView--> 
    <ImageView
        android:src="@drawable/haizewang_2"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
</com.xiaopo.flying.sticker.StickerView>
```
#### Add sticker
If the sticker is drawable, it's intrinsic width and height can not be zero.
If the sticker is text, you can set text color, font and alignment and the region which holds the text.

```java
stickerView.addSticker(sticker)
stickerView.replace(sticker)
stickerView.remove(sticker)
stickerView.removeCurrentSticker()
stickerView.removeAllStickers()
stcikerView.setLocked(true)
```

Also you can custom the icon and icon event and position

```java
 BitmapStickerIcon heartIcon =
        new BitmapStickerIcon(ContextCompat.getDrawable(this, R.drawable.ic_favorite_white_24dp),
            BitmapStickerIcon.LEFT_BOTTOM);
heartIcon.setIconEvent(new HelloIconEvent());

stickerView.setIcons(Arrays.asList(deleteIcon, zoomIcon, flipIcon, heartIcon));
```

## Todo
- [x] Constrain the sticker's moving area
- [x] Add Double Tap callback

## Licence

```
Copyright 2016 edgarmiro

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```



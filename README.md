# wallpapers

for scaling and changing exposure of wallpapers to use directly in terminal

[magick](https://imagemagick.org/)

```
bash


magick onepiece_ship_cloudy.png \

            \( -size $(identify -format "%wx%h" onepiece_ship_cloudy.png ) xc:'rgba(0,0,0,0.55)' -blur 0x15 \) -compose multiply -composite \
            \( -size $(identify -format "%wx%h" onepiece_ship_cloudy.png ) xc:'rgba(255,255,255,0.35)' -blur 0x15 \) -compose screen -composite \
            \( -size $(identify -format "%wx%h" onepiece_ship_cloudy.png ) xc:'rgba(128,0,128,0.5)' -blur 0x10 \) -compose softlight -composite \
            -modulate 100,50,100 \
            blurred/onepiece_ship_cloudy.png

magick onepiece_ship_cloudy.png -fill "rgba(0,0,0,0.65)" -draw "rectangle 0,0,9999,9999" blurred/onepiece_ship_cloudy_65.png


```


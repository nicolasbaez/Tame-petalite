# Tame-petalite
AAAH!!!

![buh](https://github.com/nicolasbaez/Tame-petalite/blob/main/xp052.gif)
```javascript
setup = (_) => createCanvas((w = 500), w, WEBGL);
k = 0;
draw = (_) => {
  colorMode(HSB, 4);
  rotateX(1);
  rotateZ(k);
  clear();
  stroke(k, 4, 4);
  noFill();
  for (i = 0; i < w; i += 2) {
    beginShape();
    for (j = 0; j < w; j += 2)
      vertex(i - w / 2, j - w / 2, (noise(i * 0.01, j * 0.01, k) * w) / 3);
    endShape();
  }
  if (k == 0) saveGif("xp052.gif", 314, { delay: 0, units: "frames" });
  k += 0.01;
};

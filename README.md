# Three.js-
总结了下用three.js遇到的坑<br>
1.做vr全景图的时候，将全景图贴在一个球上时，发现相机的位置和球的坐标都是（0,0,0），但是依然可以看到图片的内容，当时感觉很奇怪，难道说是球是透明的？
后来自己实践了下，发现实际上用了geometry.scale(-1, 1, 1);这样的话就相当于让球体的面朝内，就可以看到外部的贴图了。<br>
2.Ox颜色记忆：红绿蓝！白色为0xffffff,黑色为0x000000;<br>
3.半径为R的球体表面坐标(x,y,z)转换为Pano2VR里的tilt=arccos(Z/R)，pan=arccos(X/R)

<div align="center">
  <br>
  <h1>🎆 Fireworks Tootcart 🎆</h1>
  <p>
    <b>A <a href="https://www.lexaloffle.com/pico-8.php">PICO-8</a> fireworks display in 260 characters.</b><br />
  <sup>(<i>277 including hashtags!</i>)</sup>
  </p>
  <br>
  <p>
    <sup><a href="https://www.pico-8-edu.com/?c=AHB4YQEEAN-Hn3P06U_QXN5UwUCVFfdfflJwdhGk4RvccERSXp6mWZa-QLc-0J9zyj33ZHE58gLlWecU5_QLC2-QNY9QRDelyT0b9UOUh901UPcrh2VNb42z7qr6l4j7dKXeG5urB9p_YMFX5UCbtXnxBHHsK7tUi8nI3kYRrow0t5WPUM_MxCvpRBW_QrhVlnVpgTZ8gfskiN4hXV0oiz4RIRENkBaqwjjPNpaGR2es5hn9gLx8gbit0pkj_7nFYQ2DoCw0DAYHJkebfvQVNpc9NL1avsNkuTs1XQzMAw==&g=w-w-w-w1HQHw-w2Xw-w3Xw-w2HQH">Live demo</a>&nbsp;&nbsp;|&nbsp;&nbsp;<a href="./main.p8">Annotated code in
    <code>main.p8</code></a></sup>
  </p>
</div>

<div align="center">

![8s clip showing pixelated fireworks launching from the bottom of a 128x128 black screen, then exploding in different colours.](./firework-tootcart.gif)

</div>

```lua
l=circfill
r=rnd::_::cls()srand()for i=1,20 do
m=8+8*r()q=(t()/m)%1
x=64+q*256*(r()-.5)y=128+sin(q)*64*(r()+.8)s=sgn(sin(q+.8))l(x,y,s-1,7)j=2*(q-.2)k=m*(1-(1-j)^9)for u=0,1,.1 do
l(x+sin(u)*k,y+cos(u)*k,sin(q-.9)\1*s,q>.45 and 1 or 8+i%8)
end
end
flip()goto _
```
